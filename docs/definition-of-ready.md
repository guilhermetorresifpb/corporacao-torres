# Definition of Ready: Corporação Torres

A Definition of Ready (DoR) define os critérios que uma história de usuário precisa cumprir **antes de entrar em uma sprint**. Uma história só pode ser puxada para o planejamento quando atende a todos os itens desta lista.

> A DoR protege a sprint: evita que o time comece a trabalhar em algo mal definido e precise parar no meio para buscar informação.

---

## Critérios

### Clareza

- [ ] A história está escrita no formato: "Como [quem], quero [o quê], para [por quê]"
- [ ] O "quem" é um dos públicos definidos na visão: **Funcionário**, **Paciente** ou **Cliente**
- [ ] Os critérios de aceitação estão definidos e são verificáveis (não são ambíguos)
- [ ] O grupo sabe o que significa "done" para esta história

### Tamanho

- [ ] A história cabe em uma sprint (se for grande demais, foi quebrada em histórias menores)
- [ ] O campo **Size** está preenchido no GitHub Projects (P, M, G ou GG)

### Prioridade e contexto

- [ ] O campo **Épico** está preenchido no GitHub Projects
- [ ] O campo **MoSCoW** está preenchido (Must, Should, Could ou Won't)
- [ ] O grupo entende por que esta história está na sprint: qual problema ela resolve
- [ ] A história se conecta a pelo menos um ponto da visão do projeto (por exemplo: site de contato com direcionamento ao profissional, lista de contatos dos profissionais por área especializada, ou parcerias com prefeituras e academias)

### Dependências

- [ ] As dependências com outras histórias foram identificadas
- [ ] As histórias das quais esta depende já estão concluídas ou serão entregues antes
- [ ] Dependências externas (profissionais parceiros, prefeituras, academias, conteúdo ou dados de terceiros) foram identificadas e estão disponíveis ou têm data combinada

### Cuidados com dados de saúde

Como o projeto lida com pessoas que têm dificuldades físicas e mentais, vale checar antes de começar:

- [ ] Se a história coleta, exibe ou armazena dados pessoais ou de saúde de Pacientes ou Clientes, isso está descrito nos critérios de aceitação
- [ ] O grupo definiu quais dados são realmente necessários (coletar o mínimo possível)

---

## O que NÃO precisa estar pronto

- O design final no Figma (um wireframe de baixa fidelidade é suficiente)
- A solução técnica completamente detalhada (isso é responsabilidade de quem implementa)
- Aprovação do professor (a história está pronta quando o grupo concorda: não precisa de validação externa antes de começar)
- Acordos formais de parceria assinados (basta saber o que a história precisa do parceiro e quando)

---

## Exemplo de história que cumpre a DoR

> **Como** Paciente, **quero** preencher um formulário de contato no site informando a área em que preciso de ajuda (física ou mental), **para** ser direcionado ao profissional adequado.
>
> **Critérios de aceitação:**
> - O formulário tem os campos nome, forma de contato e área de ajuda
> - Ao enviar, o Paciente vê uma mensagem de confirmação
> - A solicitação é direcionada ao profissional da área escolhida
>
> **Size:** M · **Épico:** Contato com profissionais · **MoSCoW:** Must

---

## Observação

DoR e DoD trabalham juntas: a DoR garante que a história está pronta para começar, a DoD garante que está pronta para entregar. Se uma história entrar na sprint sem cumprir a DoR, o risco de não entregá-la aumenta significativamente.
