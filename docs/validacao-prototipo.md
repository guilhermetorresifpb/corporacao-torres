# Validação do Protótipo: Corporação Torres

## Informações gerais

- **Ferramenta:** Figma (protótipo navegável)
- **Acesso ao protótipo:** [Ver no Figma →](https://figma.com/proto/corporacao-torres-prototipo)

> Link fictício: substitua pelo link real do seu protótipo no Figma.

- **Sessões realizadas:** 2 sessões, com 3 participantes cada (total de 6)
- **Perfil dos participantes:** mix de pacientes, clientes e um funcionário administrativo, representando os três públicos-alvo do produto
- **Metodologia:** teste de usabilidade com tarefas definidas + entrevista pós-teste

---

## Tarefas testadas

1. Acessar o site e entender os serviços oferecidos pela empresa
2. Encontrar um profissional de uma área específica (ex: fisioterapeuta, educador físico)
3. Preencher o formulário de contato/solicitação de atendimento
4. Ser direcionado ao profissional correto após o envio do pedido
5. Consultar o link de contato de um profissional já direcionado

---

## Resultados por tarefa

### Tarefa 1: Entender os serviços oferecidos

| Participante | Concluiu? | Tempo    | Dificuldades                                                        |
| ------------ | --------- | -------- | --------------------------------------------------------------------- |
| P1           | Sim       | 1min 10s | Não entendeu de imediato a diferença entre "paciente" e "cliente"     |
| P2           | Sim       | 45s      | Nenhuma                                                                |
| P3           | Sim       | 1min 30s | Achou o texto inicial da home muito longo                             |
| P4           | Sim       | 50s      | Nenhuma                                                                |
| P5           | Não       | -        | Não encontrou onde clicar para ver a lista de profissionais            |
| P6           | Sim       | 1min 55s | Confundiu o menu de "Serviços" com o de "Parceiros"                   |

**Conclusão:** 5 de 6 concluíram. Principal problema: a distinção entre os públicos-alvo (paciente/cliente) e a navegação até a lista de profissionais não estavam claras.

---

### Tarefa 2: Encontrar um profissional de uma área específica

Todos os 6 participantes concluíram, mas 3 precisaram usar a busca por texto porque não identificaram os filtros por especialidade. Tempo médio: 1min 40s.

---

### Tarefa 3: Preencher o formulário de contato/solicitação

| Participante | Concluiu? | Dificuldades                                                                 |
| ------------ | --------- | ------------------------------------------------------------------------------ |
| P1           | Sim       | Nenhuma                                                                         |
| P2           | Sim       | Não sabia se precisava anexar algum documento médico                           |
| P3           | Sim       | Nenhuma                                                                         |
| P4           | Sim       | Tentou enviar o formulário sem selecionar a área de atendimento desejada       |
| P5           | Sim       | Nenhuma                                                                         |
| P6           | Não       | Desistiu por não entender qual profissional receberia o pedido                 |

**Conclusão:** Formulário funcional, mas falta clareza sobre o que acontece depois do envio e se anexos são necessários.

---

### Tarefa 4: Ser direcionado ao profissional correto

Todos concluíram. 4 participantes entenderam o direcionamento automaticamente pela área selecionada no formulário; 2 precisaram confirmar manualmente qual profissional os atenderia.

---

### Tarefa 5: Consultar o link de contato do profissional

Todos concluíram sem dificuldades. O botão/link de contato direto (WhatsApp/e-mail) foi reconhecido por todos imediatamente.

---

## Problemas identificados e ações tomadas

| # | Problema                                                      | Severidade | Ação tomada                                                                                          |
| --- | -------------------------------------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------- |
| 1 | Diferença entre "paciente" e "cliente" pouco clara na home     | Alta       | Adicionado bloco explicativo curto na página inicial diferenciando os dois perfis                        |
| 2 | Filtros de especialidade pouco visíveis na busca de profissionais | Média      | Filtros movidos para o topo da página, com ícones por área (fisioterapia, educação física, etc.)         |
| 3 | Incerteza sobre anexos no formulário de contato               | Média      | Adicionado texto no formulário: "Anexos são opcionais; se necessário, o profissional solicitará depois." |
| 4 | Falta de confirmação clara de para quem o pedido foi enviado   | Baixa      | Adicionada tela de confirmação com nome do profissional/área designada após o envio                      |

---

## Conclusão geral

O protótipo validou os fluxos principais com taxa de sucesso acima de 80% nas tarefas críticas (busca de profissional, formulário de contato e acesso ao link direto). As correções de maior impacto (diferenciação paciente/cliente e visibilidade dos filtros) foram aplicadas antes da próxima fase.

O fluxo de parcerias com prefeituras e academias ainda não foi testado no protótipo por não estar navegável nesta versão: fica como pendência para a próxima rodada de validação.