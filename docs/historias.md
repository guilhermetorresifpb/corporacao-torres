# Histórias de Usuário: Corporação Torres

As histórias estão organizadas por épico. Cada história tem critérios de aceitação que definem quando ela pode ser considerada concluída.

---

## Cadastro e Acesso

### HU001: Cadastro de cliente/paciente

**Como** pessoa interessada nos serviços da empresa,
**quero** me cadastrar no site informando meus dados básicos,
**para** poder solicitar ajuda física ou mental.

**Critérios de aceitação:**

- O sistema solicita nome, e-mail, telefone e tipo de necessidade (física, mental ou ambas)
- O e-mail deve ser único no sistema
- A senha deve ter no mínimo 8 caracteres
- Após o cadastro, o usuário recebe um e-mail de confirmação

---

### HU002: Cadastro de profissional parceiro

**Como** profissional de saúde ou educação física,
**quero** me cadastrar como parceiro da empresa,
**para** poder atender clientes e pacientes encaminhados.

**Critérios de aceitação:**

- O sistema solicita nome, especialidade, registro profissional (CRM, CREF, CRP etc.) e contato
- O cadastro só é ativado após aprovação de um funcionário responsável
- O profissional recebe notificação sobre a aprovação ou recusa

---

### HU003: Login

**Como** usuário cadastrado (funcionário, profissional, cliente ou paciente),
**quero** fazer login com e-mail e senha,
**para** acessar minha área na plataforma.

**Critérios de aceitação:**

- O sistema valida e-mail e senha
- Em caso de erro, exibe mensagem genérica (sem informar qual campo está errado)
- Cada tipo de usuário é redirecionado para sua respectiva área após o login

---

## Contato e Encaminhamento

### HU004: Solicitar ajuda pelo site

**Como** cliente ou paciente,
**quero** preencher um formulário de contato descrevendo minha necessidade,
**para** ser encaminhado ao profissional adequado.

**Critérios de aceitação:**

- O formulário pede nome, contato, área desejada (física ou mental) e uma breve descrição
- Após o envio, o cliente recebe uma confirmação de que o pedido foi registrado
- O pedido fica visível para os funcionários responsáveis pelo encaminhamento

---

### HU005: Ver lista de profissionais por especialidade

**Como** cliente ou paciente,
**quero** visualizar os profissionais disponíveis organizados por área,
**para** escolher com quem entrar em contato.

**Critérios de aceitação:**

- O site exibe os profissionais agrupados por especialidade (ex: nutrição, psicologia, educação física)
- Cada profissional mostra nome, especialidade e link de contato (WhatsApp, e-mail ou telefone)
- Apenas profissionais aprovados aparecem na lista

---

### HU006: Encaminhar pedido a um profissional

**Como** funcionário,
**quero** direcionar um pedido de cliente ou paciente ao profissional mais adequado,
**para** garantir que ele seja atendido corretamente.

**Critérios de aceitação:**

- O funcionário visualiza a lista de pedidos pendentes
- O funcionário escolhe um profissional compatível com a necessidade descrita
- O profissional e o cliente/paciente são notificados do encaminhamento

---

## Área do Funcionário

### HU007: Painel de pedidos pendentes

**Como** funcionário,
**quero** ver todos os pedidos de ajuda ainda não encaminhados,
**para** organizar o atendimento de forma profissional.

**Critérios de aceitação:**

- Os pedidos aparecem ordenados do mais antigo para o mais recente
- Cada pedido mostra nome do solicitante, área desejada e descrição
- O funcionário pode marcar um pedido como "em andamento" ou "encaminhado"

---

### HU008: Aprovar cadastro de profissional

**Como** funcionário responsável,
**quero** analisar e aprovar ou recusar o cadastro de novos profissionais,
**para** garantir que apenas profissionais qualificados atendam pela plataforma.

**Critérios de aceitação:**

- O funcionário visualiza os dados e o registro profissional enviado
- Ao aprovar, o profissional passa a aparecer na lista pública de contatos
- Ao recusar, o sistema exige um motivo, enviado ao profissional

---

## Parcerias

### HU009: Cadastrar parceria com prefeitura ou academia

**Como** funcionário administrativo,
**quero** registrar uma nova parceria firmada,
**para** manter o controle de quem pode encaminhar ou receber pacientes parceiros.

**Critérios de aceitação:**

- O sistema solicita nome da instituição parceira, tipo (prefeitura ou academia) e contato responsável
- A parceria fica registrada com data de início
- Pedidos vindos de uma parceria são identificados como tal no painel de pedidos

---

### HU010: Listar parcerias ativas

**Como** funcionário,
**quero** visualizar todas as parcerias ativas da empresa,
**para** acompanhar quais instituições estão colaborando no momento.

**Critérios de aceitação:**

- A lista exibe nome, tipo e status (ativa ou encerrada) de cada parceria
- É possível filtrar por tipo de parceria (prefeitura ou academia)

---

## Site Institucional

### HU011: Página de apresentação da empresa

**Como** visitante do site,
**quero** entender o que a Corporação Torres oferece,
**para** decidir se quero solicitar ajuda ou contato.

**Critérios de aceitação:**

- A página apresenta a missão da empresa e os tipos de ajuda oferecidos (física e mental)
- A página exibe um botão de destaque para "Solicitar ajuda" ou "Entrar em contato"
- A página é acessível sem necessidade de login

---

### HU012: Contato institucional

**Como** visitante do site,
**quero** encontrar os canais de contato da empresa,
**para** falar diretamente com a Corporação Torres.

**Critérios de aceitação:**

- O site exibe WhatsApp Business, e-mail institucional e formulário de contato
- Todos os canais estão visíveis na mesma seção de contato
- O formulário envia a mensagem para o e-mail institucional da empresa