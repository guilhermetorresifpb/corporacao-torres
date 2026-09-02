# ADR 002: Escolha do Banco de Dados

- **Status:** Proposto
- **Data:** [preencher data]

---

## Contexto

Com a stack definida em [ADR 001](./001-escolha-de-stack.md), precisávamos escolher o banco de dados para a Corporação Torres. A aplicação precisa lidar com:

- Dados estruturados com relacionamentos claros entre entidades: funcionários, profissionais, pacientes, clientes, agendamentos e parcerias
- Cadastro e histórico de atendimentos vinculados a pacientes/clientes específicos
- Contatos direcionados por área de especialização (site indica o profissional correto)
- Volume inicial pequeno (empresa começando em formato home office)
- Sem necessidade de escala horizontal no curto prazo

---

## Decisão

Usaremos **PostgreSQL 15+** como banco de dados relacional principal.

O acesso ao banco será feito via um ORM (ex: Prisma, Sequelize ou equivalente, dependendo da stack escolhida em ADR 001), com migrações versionadas para controlar mudanças no esquema ao longo do crescimento da empresa.

---

## Alternativas consideradas

### PostgreSQL vs. MySQL

- **PostgreSQL** foi escolhido por ter melhor conformidade com o padrão SQL, suporte nativo a tipos avançados (JSON, arrays) que podem ser úteis para armazenar informações variáveis de atendimentos, e boa integração com plataformas de hospedagem populares.
- **MySQL** foi descartado por não trazer vantagem clara para o caso de uso da Corporação Torres.

### PostgreSQL vs. MongoDB

- **MongoDB** foi considerado pela flexibilidade em armazenar registros variados de atendimentos.
- Descartado porque as relações centrais do sistema (paciente ↔ profissional ↔ agendamento ↔ parceria) são fortemente relacionais; modelar isso em um banco não-relacional aumentaria a complexidade da lógica de negócio sem necessidade real no estágio atual da empresa.

---

## Modelo de dados resumido
usuarios
id, nome, email, senha_hash, tipo (funcionario, profissional), created_at

profissionais
id, usuario_id (FK), area_especializacao, contato, ativo

pacientes
id, nome, email, telefone, created_at

clientes
id, nome, email, telefone, created_at

agendamentos
id, paciente_id (FK, opcional), cliente_id (FK, opcional), profissional_id (FK), data_hora, status, created_at

parcerias
id, nome_instituicao, tipo (prefeitura, academia), contato, ativo

---

## Consequências

**Positivas:**

- Modelo relacional cobre bem o fluxo de direcionamento de pacientes/clientes aos profissionais certos
- PostgreSQL tem suporte amplo em serviços de hospedagem gratuitos/baratos, adequado para o estágio inicial (home office)
- Facilita relatórios futuros (ex: quantos atendimentos por área, por parceria)

**Negativas / Riscos:**

- Consultas de agenda por profissional podem ficar lentas sem índices adequados conforme a base cresce
- Mitigação: adicionar índices em `agendamentos(profissional_id, data_hora)` desde o início

---

## Revisão

Revisitar esta decisão se o volume de pacientes/clientes crescer significativamente com a transição para atendimento presencial, ou se surgir necessidade de recursos que o PostgreSQL não atenda bem (ex: buscas complexas de texto livre em prontuários).