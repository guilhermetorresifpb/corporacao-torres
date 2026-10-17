# Histórias de Usuário: Corporação Torres

As histórias estão organizadas por épico. Cada história tem critérios de aceitação que definem quando ela pode ser considerada concluída.

Perfis de usuário (conforme a [visão](visao.md)):

- **Cliente:** pessoa que tem acesso aos serviços da empresa.
- **Paciente:** pessoa que recebe apoio da empresa e dos parceiros.
- **Funcionário:** pessoa da empresa que atende os pedidos de clientes e pacientes.

---

## Cadastro e Acesso

### HU001: Cadastro de cliente ou paciente

**Como** cliente ou paciente,  
**quero** criar uma conta no site da Corporação Torres,  
**para** solicitar ajuda e serviços da empresa.

**Critérios de aceitação:**

- O usuário informa nome, e-mail, telefone e senha
- O usuário escolhe se é cliente ou paciente
- A senha deve ter no mínimo 8 caracteres
- O e-mail deve ser único no sistema
- O sistema exibe mensagem de sucesso após o cadastro

---

### HU002: Login

**Como** usuário cadastrado,  
**quero** fazer login com e-mail e senha,  
**para** acessar minha conta e acompanhar minhas solicitações.

**Critérios de aceitação:**

- O sistema valida e-mail e senha
- Em caso de erro, exibe mensagem genérica (sem informar qual campo está errado)
- Após login bem-sucedido, o usuário é redirecionado para a página inicial da sua área
- A sessão é mantida até o logout explícito

---

### HU003: Logout

**Como** usuário logado,  
**quero** fazer logout,  
**para** sair da minha conta com segurança.

**Critérios de aceitação:**

- O botão de logout está acessível em qualquer página após login
- Após logout, a sessão é encerrada
- O usuário é redirecionado para a tela de login

---

### HU004: Login de funcionário

**Como** funcionário da empresa,  
**quero** acessar uma área exclusiva de atendimento,  
**para** gerenciar os pedidos de clientes e pacientes.

**Critérios de aceitação:**

- Contas de funcionário são criadas apenas por um administrador
- Funcionários acessam um painel que clientes e pacientes não conseguem ver
- Em caso de erro no login, exibe mensagem genérica

---

## Solicitação de Ajuda

### HU005: Solicitar ajuda ou serviço

**Como** cliente ou paciente,  
**quero** enviar um pedido de ajuda pelo site,  
**para** ser direcionado ao profissional adequado.

**Critérios de aceitação:**

- O usuário seleciona a área do pedido (ex: saúde física, saúde mental, educação física)
- O usuário descreve a necessidade em um campo de texto (máx. 1.000 caracteres)
- O pedido não pode ser enviado com a descrição vazia
- O sistema exibe mensagem de confirmação após o envio
- O pedido fica registrado com data e hora

---

### HU006: Acompanhar status do pedido

**Como** cliente ou paciente,  
**quero** ver o andamento dos meus pedidos,  
**para** saber se já estou sendo atendido.

**Critérios de aceitação:**

- A lista mostra todos os pedidos do usuário, do mais recente para o mais antigo
- Cada pedido exibe a área, a data e o status (Recebido, Em atendimento, Concluído)
- O usuário só vê os próprios pedidos

---

### HU007: Cancelar pedido

**Como** cliente ou paciente,  
**quero** cancelar um pedido que ainda não foi atendido,  
**para** desistir da solicitação quando não precisar mais.

**Critérios de aceitação:**

- Só é possível cancelar pedidos com status "Recebido"
- O sistema pede confirmação antes de cancelar
- Após o cancelamento, o status do pedido muda para "Cancelado"

---

## Profissionais

### HU008: Ver profissionais por área

**Como** cliente ou paciente,  
**quero** ver a lista de profissionais de cada área especializada,  
**para** escolher quem pode me ajudar.

**Critérios de aceitação:**

- A lista pode ser filtrada por área (médicos, profissionais de educação física, etc.)
- Cada profissional exibe nome, área de atuação e foto
- A lista é acessível sem necessidade de login

---

### HU009: Acessar link de contato do profissional

**Como** cliente ou paciente,  
**quero** acessar o link de contato de um profissional,  
**para** falar diretamente com ele.

**Critérios de aceitação:**

- Cada profissional possui um link de contato visível no seu card
- O link abre em uma nova aba
- Se o profissional não tiver link cadastrado, o card exibe a mensagem "Contato indisponível"

---

### HU010: Cadastrar profissional

**Como** funcionário,  
**quero** cadastrar um novo profissional parceiro,  
**para** que ele apareça na lista do site.

**Critérios de aceitação:**

- O funcionário informa nome, área de atuação, foto e link de contato
- Nome e área são obrigatórios
- O profissional cadastrado aparece imediatamente na lista pública

---

### HU011: Editar e remover profissional

**Como** funcionário,  
**quero** editar ou remover um profissional da lista,  
**para** manter as informações sempre atualizadas.

**Critérios de aceitação:**

- Apenas funcionários podem editar ou remover profissionais
- O sistema pede confirmação antes de remover
- As alterações aparecem imediatamente na lista pública

---

## Atendimento (Funcionários)

### HU012: Ver pedidos recebidos

**Como** funcionário,  
**quero** ver todos os pedidos de clientes e pacientes,  
**para** atendê-los de forma profissional.

**Critérios de aceitação:**

- A lista mostra pedidos do mais antigo para o mais recente, priorizando os ainda não atendidos
- Cada pedido exibe nome do solicitante, área, descrição, data e status
- A lista pode ser filtrada por status e por área
- A lista é paginada (20 pedidos por página)

---

### HU013: Direcionar pedido ao profissional

**Como** funcionário,  
**quero** direcionar um pedido ao profissional da área correspondente,  
**para** que o cliente ou paciente receba o atendimento adequado.

**Critérios de aceitação:**

- O funcionário seleciona um profissional da mesma área do pedido
- Após o direcionamento, o status muda para "Em atendimento"
- O solicitante consegue ver o profissional responsável no seu pedido

---

### HU014: Concluir pedido

**Como** funcionário,  
**quero** marcar um pedido como concluído,  
**para** registrar que o cliente ou paciente foi atendido.

**Critérios de aceitação:**

- Apenas funcionários podem concluir pedidos
- Apenas pedidos "Em atendimento" podem ser concluídos
- O status muda para "Concluído" e o solicitante vê a atualização

---

## Parcerias

### HU015: Ver parceiros da empresa

**Como** cliente ou paciente,  
**quero** ver as prefeituras e academias parceiras,  
**para** saber onde posso conseguir ajuda.

**Critérios de aceitação:**

- A página exibe a lista de parceiros com nome, tipo (prefeitura ou academia) e descrição
- A lista pode ser filtrada por tipo
- A página é acessível sem necessidade de login

---

### HU016: Gerenciar parceiros

**Como** funcionário,  
**quero** cadastrar, editar e remover parceiros,  
**para** manter a página de parcerias atualizada.

**Critérios de aceitação:**

- O funcionário informa nome, tipo e descrição do parceiro
- Apenas funcionários podem gerenciar parceiros
- O sistema pede confirmação antes de remover
- As alterações aparecem imediatamente na página pública

---

## Informações da Empresa

### HU017: Conhecer a empresa

**Como** visitante do site,  
**quero** ler sobre a proposta e o impacto da Corporação Torres,  
**para** entender como a empresa pode me ajudar.

**Critérios de aceitação:**

- A página inicial apresenta a proposta da empresa
- A página explica para quem a empresa atende (funcionários, pacientes e clientes)
- Há um botão de destaque para "Solicitar ajuda"
- A página é acessível sem necessidade de login
