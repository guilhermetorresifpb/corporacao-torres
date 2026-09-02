# ADR 001: Escolha de Stack Tecnológica — Site Corporação Torres

- **Status:** Proposto
- **Data:** [preencher data]

---

## Contexto

O site da Corporação Torres precisa apresentar a empresa e direcionar clientes e pacientes aos profissionais de cada área (física e mental), com contato por formulário, WhatsApp Business e e-mail institucional. A escolha da stack precisa levar em conta:

- Projeto começa em formato home office, com orçamento enxuto
- Site simples (institucional + contato), sem necessidade de sistema complexo por trás no início
- Facilidade de manutenção por uma pessoa só (ou equipe pequena)
- Possibilidade de evoluir depois (ex.: agendamento, área de paciente) sem reescrever tudo

---

## Decisão

Adotaremos a seguinte stack:

| Camada | Tecnologia | Observação |
| --- | --- | --- |
| Frontend | HTML + CSS + JavaScript (ou React, se quiser componentizar) | Site institucional estático |
| Formulário de contato | Serviço de formulário (ex.: Formspree, Web3Forms) ou backend simples | Evita montar servidor próprio no início |
| Hospedagem | Netlify ou Vercel (plano gratuito) | Deploy automático a partir do Git |
| Domínio | Registro próprio (ex.: registro.br) | corporacaotorres.com.br ou similar |
| Controle de versão | Git + GitHub | Histórico e backup do código |

---

## Alternativas consideradas

### Frontend: site estático vs. React vs. WordPress

- **HTML/CSS/JS estático** foi escolhido por ser suficiente para um site de apresentação + contato, rápido de carregar e barato de manter.
- **React** foi considerado para o caso de o site crescer (área logada, painel de profissionais), mas adiciona complexidade desnecessária na fase inicial.
- **WordPress** foi descartado por exigir hospedagem paga e manutenção de plugins/segurança, o que não compensa para um site simples.

### Formulário de contato: serviço externo vs. backend próprio

- **Serviço externo (Formspree/Web3Forms)** foi escolhido por eliminar a necessidade de manter servidor e banco de dados só para receber mensagens.
- **Backend próprio (Node/PHP)** foi descartado por enquanto, mas fica como opção natural quando o site evoluir para agendamento ou cadastro de pacientes.

### Hospedagem: Netlify/Vercel vs. hospedagem tradicional paga

- **Netlify/Vercel** foram escolhidos pelo plano gratuito, deploy automático via Git e certificado HTTPS incluído.
- **Hospedagem paga tradicional** foi descartada por enquanto, por gerar custo fixo sem necessidade no estágio atual do projeto.

---

## Consequências

**Positivas:**

- Custo inicial baixo (hospedagem e formulário gratuitos)
- Deploy simples: qualquer atualização no Git já atualiza o site
- Baixa curva de aprendizado, permite que você mesmo mantenha o site

**Negativas / Riscos:**

- Site estático tem limitações se o projeto crescer (ex.: login de paciente, agendamento online)
- Depender de serviço externo de formulário significa ficar sujeito aos limites do plano gratuito
- Vai exigir migração de stack no futuro se a empresa precisar de sistema mais robusto (ex.: prontuário, agenda integrada)

---

## Revisão

Esta decisão será revisada quando o site precisar de funcionalidades além de apresentação e contato (ex.: agendamento, área do paciente, painel administrativo).