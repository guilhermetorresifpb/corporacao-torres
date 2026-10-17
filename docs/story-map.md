# Story Map: Corporação Torres

## Acesso ao mapa

O story map completo pode ser montado em uma ferramenta visual (Miro, FigJam, etc.).
> Link pendente: adicione aqui o link do seu board quando criá-lo.

---

## Estrutura do mapa

O mapa está organizado em 3 linhas:

| Linha                          | O que representa                                                     |
| ------------------------------ | -------------------------------------------------------------------- |
| **Atividades** (linha do topo) | O que o usuário faz em alto nível                                    |
| **Tarefas** (linha do meio)    | As ações específicas dentro de cada atividade                        |
| **Histórias** (linhas abaixo)  | As histórias de usuário, ordenadas por prioridade de cima para baixo |

---

## Atores

Baseados no público-alvo definido na [visão](visao.md):

| Ator             | Descrição                                                                    |
| ---------------- | ---------------------------------------------------------------------------- |
| **Cliente**      | Pessoa que busca os serviços da empresa                                      |
| **Paciente**     | Pessoa que recebe apoio da empresa e dos parceiros                           |
| **Funcionário**  | Atende os pedidos de clientes e pacientes e os direciona ao profissional     |

---

## Atividades mapeadas

1. **Conhecer a empresa**: Entender a proposta, o impacto e as áreas de atendimento
2. **Pedir ajuda**: Entrar em contato pelo site e solicitar atendimento
3. **Encontrar profissionais**: Consultar os contatos dos profissionais de cada área especializada
4. **Atender pedidos**: Receber pedidos e direcioná-los ao profissional adequado (funcionário)
5. **Gerenciar profissionais e parceiros**: Manter atualizados os profissionais, as prefeituras e as academias parceiras (funcionário)

---

## Tarefas e histórias por atividade

### 1. Conhecer a empresa

| Tarefa                         | Histórias                                      |
| ------------------------------ | ---------------------------------------------- |
| Ver quem somos                 | HU001: Ver apresentação da empresa             |
| Ver áreas de atendimento       | HU002: Ver áreas de atendimento (física e mental) |
| Ver parceiros                  | HU014: Ver prefeituras e academias parceiras   |

### 2. Pedir ajuda

| Tarefa                         | Histórias                                      |
| ------------------------------ | ---------------------------------------------- |
| Enviar pedido de contato       | HU003: Enviar pedido de ajuda pelo site        |
| Informar a área desejada       | HU004: Escolher a área de atendimento no pedido |
| Acompanhar o pedido            | HU013: Acompanhar status do pedido             |

### 3. Encontrar profissionais

| Tarefa                         | Histórias                                      |
| ------------------------------ | ---------------------------------------------- |
| Ver contatos por área          | HU005: Ver links de contato dos profissionais por área |
| Ver detalhes do profissional   | HU006: Ver perfil do profissional              |
| Buscar profissional            | HU016: Buscar profissional por especialidade   |

### 4. Atender pedidos

| Tarefa                         | Histórias                                      |
| ------------------------------ | ---------------------------------------------- |
| Entrar no painel               | HU007: Login de funcionário                    |
| Ver pedidos recebidos          | HU008: Listar pedidos recebidos                |
| Direcionar ao profissional     | HU009: Direcionar pedido ao profissional       |
| Atualizar andamento            | HU010: Atualizar status do pedido              |

### 5. Gerenciar profissionais e parceiros

| Tarefa                         | Histórias                                      |
| ------------------------------ | ---------------------------------------------- |
| Cadastrar profissional         | HU011: Cadastrar profissional                  |
| Manter profissional            | HU012: Editar e remover profissional           |
| Cadastrar parceiro             | HU015: Cadastrar parceiro (prefeitura/academia) |

---

## Definição do MVP

O MVP da Corporação Torres cobre o fluxo essencial para que um cliente ou paciente conheça a empresa, peça ajuda pelo site e seja direcionado ao profissional certo.

**Histórias incluídas no MVP:**

| História | Descrição                                          |
| -------- | -------------------------------------------------- |
| HU001    | Ver apresentação da empresa                        |
| HU002    | Ver áreas de atendimento (física e mental)         |
| HU003    | Enviar pedido de ajuda pelo site                   |
| HU004    | Escolher a área de atendimento no pedido           |
| HU005    | Ver links de contato dos profissionais por área    |
| HU007    | Login de funcionário                               |
| HU008    | Listar pedidos recebidos                           |
| HU009    | Direcionar pedido ao profissional                  |
| HU010    | Atualizar status do pedido                         |

**Histórias fora do MVP (incremento seguinte):**

| História | Descrição                                          |
| -------- | -------------------------------------------------- |
| HU006    | Ver perfil do profissional                         |
| HU011    | Cadastrar profissional                             |
| HU012    | Editar e remover profissional                      |
| HU013    | Acompanhar status do pedido                        |
| HU014    | Ver prefeituras e academias parceiras              |
| HU015    | Cadastrar parceiro (prefeitura/academia)           |
| HU016    | Buscar profissional por especialidade              |

---

## Critério de MVP

O MVP foi definido com base na pergunta:
> *"O que o usuário precisa fazer no mínimo para que a plataforma tenha valor para ele?"*

A resposta foi: **conhecer a empresa, pedir ajuda e ser direcionado a um profissional.** Isso corresponde ao "Alto Nível" da visão: um site para clientes e pacientes entrarem em contato, que direciona ao profissional, com links de contato por área. No MVP, os links dos profissionais podem ser mantidos de forma simples (lista fixa), e o cadastro e a gestão de profissionais e parceiros ficam para o incremento seguinte.
