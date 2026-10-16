# Backlog de Exemplo: Corporação Torres

Este documento mostra como popular o GitHub Projects da Corporação Torres. Cada seção abaixo representa um Issue no board, com os campos customizados e o checklist de tasks técnicas que ficam dentro do issue.

Personas usadas nas histórias, conforme o documento de visão: **cliente**, **paciente** e **funcionário**.

---

## Visão geral do backlog

| ID    | Épico                | MoSCoW | Size | Sprint   |
| ----- | -------------------- | ------ | ---- | -------- |
| HU001 | Site institucional   | Must   | P    | Sprint 1 |
| HU002 | Site institucional   | Must   | M    | Sprint 1 |
| HU003 | Profissionais        | Must   | M    | Sprint 1 |
| HU004 | Profissionais        | Must   | P    | Sprint 1 |
| HU005 | Profissionais        | Must   | M    | Sprint 2 |
| HU007 | Autenticação         | Must   | G    | Sprint 2 |
| HU008 | Autenticação         | Must   | P    | Sprint 2 |
| HU009 | Autenticação         | Must   | P    | Sprint 2 |
| HU010 | Autenticação         | Must   | M    | Sprint 2 |
| HU011 | Pedidos de ajuda     | Must   | G    | Sprint 3 |
| HU012 | Pedidos de ajuda     | Must   | M    | Sprint 3 |
| HU013 | Pedidos de ajuda     | Must   | M    | Sprint 3 |
| HU006 | Profissionais        | Should | P    | Sprint 3 |
| HU014 | Pedidos de ajuda     | Should | M    | Sprint 4 |
| HU015 | Pedidos de ajuda     | Should | P    | Sprint 4 |
| HU016 | Parcerias            | Should | P    | Sprint 4 |
| HU017 | Parcerias            | Should | M    | Sprint 4 |
| HU018 | Profissionais        | Could  | M    | Sprint 4 |

---

## Issues detalhados

---

### HU001: Ver página inicial da empresa

**Épico:** Site institucional | **MoSCoW:** Must | **Size:** P | **Sprint:** Sprint 1
> Como cliente ou paciente, quero ver a página inicial da Corporação Torres, para entender como a empresa pode me ajudar na parte física e mental.

**Tasks:**

- [ ] Criar a página inicial com a proposta da empresa (ajuda física e mental com médicos e profissionais de educação física)
- [ ] Exibir botão de destaque "Pedir ajuda" que leva ao formulário de contato
- [ ] Criar header com navegação (Início, Profissionais, Parceiros, Entrar)
- [ ] Criar rodapé com informações de contato da empresa
- [ ] Garantir layout responsivo para celular

---

### HU002: Ver áreas de atendimento

**Épico:** Site institucional | **MoSCoW:** Must | **Size:** M | **Sprint:** Sprint 1
> Como cliente ou paciente, quero ver as áreas especializadas atendidas pela empresa, para saber qual tipo de profissional procurar.

**Tasks:**

- [ ] Criar migration da tabela `areas` (id, nome, descricao)
- [ ] Criar endpoint `GET /areas` que lista as áreas especializadas
- [ ] Criar página/seção que exibe as áreas em cards (ex: ortopedia, psicologia, educação física)
- [ ] Ao clicar em uma área, levar para a lista de profissionais daquela área

---

### HU003: Ver profissionais por área

**Épico:** Profissionais | **MoSCoW:** Must | **Size:** M | **Sprint:** Sprint 1
> Como cliente ou paciente, quero ver os profissionais de cada área especializada, para escolher com quem entrar em contato.

**Tasks:**

- [ ] Criar migration da tabela `professionals` (id, nome, area_id, descricao, link_contato, ativo)
- [ ] Criar endpoint `GET /professionals?area=...` com filtro por área
- [ ] Criar página de listagem de profissionais com nome, área e descrição
- [ ] Exibir mensagem quando não houver profissionais cadastrados na área

---

### HU004: Acessar link de contato do profissional

**Épico:** Profissionais | **MoSCoW:** Must | **Size:** P | **Sprint:** Sprint 1
> Como cliente ou paciente, quero acessar o link de contato de um profissional, para falar diretamente com ele.

**Tasks:**

- [ ] Exibir botão "Entrar em contato" em cada card de profissional
- [ ] Abrir o link de contato (WhatsApp, e-mail ou outro) em nova aba
- [ ] Validar que o link cadastrado é uma URL válida antes de exibir
- [ ] Ocultar o botão quando o profissional não tiver link cadastrado

---

### HU005: Cadastrar profissional

**Épico:** Profissionais | **MoSCoW:** Must | **Size:** M | **Sprint:** Sprint 2
> Como funcionário da empresa, quero cadastrar um profissional parceiro, para que ele apareça no site para clientes e pacientes.

**Tasks:**

- [ ] Criar endpoint `POST /professionals` restrito a funcionários
- [ ] Validar campos obrigatórios (nome, área, link de contato)
- [ ] Criar formulário de cadastro de profissional na área do funcionário
- [ ] Exibir mensagem de sucesso e redirecionar para a lista de profissionais
- [ ] Tratar e exibir erros de validação no formulário

---

### HU007: Cadastro de cliente ou paciente

**Épico:** Autenticação | **MoSCoW:** Must | **Size:** G | **Sprint:** Sprint 2
> Como cliente ou paciente, quero criar uma conta, para fazer pedidos de ajuda e acompanhar o atendimento.

**Tasks:**

- [ ] Criar migration da tabela `users` (id, nome, email, telefone, password_hash, perfil, created_at)
- [ ] Criar endpoint `POST /auth/register`
- [ ] Aplicar hash de senha com bcrypt antes de salvar
- [ ] Validar e-mail único e senha com requisito mínimo de segurança
- [ ] Criar página de cadastro com formulário (nome, e-mail, telefone, senha, tipo: cliente ou paciente)
- [ ] Tratar e exibir erros: e-mail já cadastrado, senha fraca, campos vazios
- [ ] Exibir mensagem de sucesso e redirecionar para o login

---

### HU008: Login

**Épico:** Autenticação | **MoSCoW:** Must | **Size:** P | **Sprint:** Sprint 2
> Como usuário cadastrado, quero fazer login com e-mail e senha, para acessar minha conta.

**Tasks:**

- [ ] Criar endpoint `POST /auth/login` que valida credenciais e retorna JWT
- [ ] Configurar expiração do token (ex: 7 dias)
- [ ] Criar página de login com formulário (e-mail, senha)
- [ ] Armazenar o token após login bem-sucedido
- [ ] Redirecionar para a página inicial após login
- [ ] Exibir mensagem de erro genérica em caso de credenciais inválidas

---

### HU009: Logout

**Épico:** Autenticação | **MoSCoW:** Must | **Size:** P | **Sprint:** Sprint 2
> Como usuário logado, quero fazer logout, para sair da minha conta com segurança.

**Tasks:**

- [ ] Criar botão de logout acessível no header em todas as páginas
- [ ] Remover o token armazenado ao clicar em logout
- [ ] Redirecionar para a página de login
- [ ] Garantir que rotas protegidas redirecionam para login se não houver token válido

---

### HU010: Acesso diferenciado para funcionários

**Épico:** Autenticação | **MoSCoW:** Must | **Size:** M | **Sprint:** Sprint 2
> Como funcionário da empresa, quero ter uma área de acesso própria, para gerenciar profissionais e atender os pedidos dos clientes e pacientes.

**Tasks:**

- [ ] Adicionar o campo `perfil` (cliente, paciente, funcionario) e usá-lo nas permissões
- [ ] Criar middleware que bloqueia endpoints de gestão para quem não é funcionário
- [ ] Criar área restrita do funcionário (menu e rotas protegidas)
- [ ] Exibir menu diferente conforme o perfil do usuário logado
- [ ] Retornar erro 403 ao tentar acessar área restrita sem permissão

---

### HU011: Enviar pedido de ajuda

**Épico:** Pedidos de ajuda | **MoSCoW:** Must | **Size:** G | **Sprint:** Sprint 3
> Como cliente ou paciente, quero enviar um pedido de ajuda descrevendo minha necessidade, para que a empresa me direcione ao profissional certo.

**Tasks:**

- [ ] Criar migration da tabela `requests` (id, user_id, area_id, descricao, status, created_at)
- [ ] Criar endpoint `POST /requests`
- [ ] Definir status inicial `pendente` ao criar o pedido
- [ ] Criar formulário de pedido (área desejada, descrição da necessidade)
- [ ] Validar campos obrigatórios e limite de caracteres da descrição
- [ ] Exibir mensagem de confirmação após o envio
- [ ] Exigir login para enviar o pedido

---

### HU012: Ver pedidos recebidos

**Épico:** Pedidos de ajuda | **MoSCoW:** Must | **Size:** M | **Sprint:** Sprint 3
> Como funcionário da empresa, quero ver os pedidos de clientes e pacientes, para atendê-los de forma profissional.

**Tasks:**

- [ ] Criar endpoint `GET /requests` restrito a funcionários, com filtro por status e área
- [ ] Ordenar pedidos do mais antigo para o mais recente
- [ ] Criar página de listagem de pedidos na área do funcionário
- [ ] Exibir nome do solicitante, área, descrição e status em cada pedido
- [ ] Criar página de detalhes do pedido

---

### HU013: Direcionar pedido ao profissional

**Épico:** Pedidos de ajuda | **MoSCoW:** Must | **Size:** M | **Sprint:** Sprint 3
> Como funcionário da empresa, quero direcionar um pedido ao profissional da área correta, para que o paciente ou cliente receba o atendimento adequado.

**Tasks:**

- [ ] Adicionar o campo `professional_id` na tabela `requests`
- [ ] Criar endpoint `PUT /requests/{id}/assign` que vincula o pedido a um profissional
- [ ] Listar apenas profissionais da área do pedido na hora de direcionar
- [ ] Exibir o link de contato do profissional para o funcionário repassar
- [ ] Atualizar o status do pedido para `direcionado`

---

### HU006: Editar ou remover profissional

**Épico:** Profissionais | **MoSCoW:** Should | **Size:** P | **Sprint:** Sprint 3
> Como funcionário da empresa, quero editar ou remover um profissional, para manter a lista do site sempre atualizada.

**Tasks:**

- [ ] Criar endpoint `PUT /professionals/{id}` restrito a funcionários
- [ ] Criar endpoint `DELETE /professionals/{id}` (ou marcar como inativo)
- [ ] Exibir ações de editar e remover na lista da área do funcionário
- [ ] Exibir modal de confirmação antes de remover
- [ ] Garantir que profissionais inativos não aparecem no site público

---

### HU014: Acompanhar status do pedido

**Épico:** Pedidos de ajuda | **MoSCoW:** Should | **Size:** M | **Sprint:** Sprint 4
> Como paciente ou cliente, quero acompanhar o status dos meus pedidos, para saber se já fui direcionado a um profissional.

**Tasks:**

- [ ] Criar endpoint `GET /requests/me` que retorna os pedidos do usuário logado
- [ ] Criar página "Meus pedidos" com lista e status (pendente, direcionado, concluído)
- [ ] Exibir o profissional responsável quando o pedido já tiver sido direcionado
- [ ] Exibir mensagem quando o usuário ainda não tiver pedidos

---

### HU015: Atualizar status do pedido

**Épico:** Pedidos de ajuda | **MoSCoW:** Should | **Size:** P | **Sprint:** Sprint 4
> Como funcionário da empresa, quero atualizar o status de um pedido, para manter o cliente ou paciente informado.

**Tasks:**

- [ ] Criar endpoint `PUT /requests/{id}/status` restrito a funcionários
- [ ] Validar os status permitidos (pendente, direcionado, concluído, cancelado)
- [ ] Adicionar seletor de status na página de detalhes do pedido
- [ ] Refletir a mudança imediatamente na lista de pedidos

---

### HU016: Ver parceiros da empresa

**Épico:** Parcerias | **MoSCoW:** Should | **Size:** P | **Sprint:** Sprint 4
> Como cliente ou paciente, quero ver as prefeituras e academias parceiras, para saber onde posso receber apoio.

**Tasks:**

- [ ] Criar endpoint `GET /partners` com filtro por tipo (prefeitura ou academia)
- [ ] Criar página pública de parceiros com nome, tipo, cidade e contato
- [ ] Exibir mensagem quando não houver parceiros cadastrados

---

### HU017: Cadastrar parceiro

**Épico:** Parcerias | **MoSCoW:** Should | **Size:** M | **Sprint:** Sprint 4
> Como funcionário da empresa, quero cadastrar prefeituras e academias parceiras, para que apareçam no site.

**Tasks:**

- [ ] Criar migration da tabela `partners` (id, nome, tipo, cidade, contato, ativo)
- [ ] Criar endpoint `POST /partners` restrito a funcionários
- [ ] Criar formulário de cadastro de parceiro na área do funcionário
- [ ] Validar campos obrigatórios e o tipo do parceiro
- [ ] Exibir o novo parceiro na lista pública após o cadastro

---

### HU018: Buscar profissional por nome

**Épico:** Profissionais | **MoSCoW:** Could | **Size:** M | **Sprint:** Sprint 4
> Como cliente ou paciente, quero buscar um profissional pelo nome, para encontrá-lo rapidamente sem navegar por todas as áreas.

**Tasks:**

- [ ] Criar endpoint `GET /professionals/search?q=...` com busca parcial por nome
- [ ] Criar barra de busca no header
- [ ] Exibir resultados conforme o usuário digita (debounce de 300ms)
- [ ] Exibir mensagem quando nenhum profissional for encontrado
