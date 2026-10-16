# Definition of Done: Corporação Torres

A Definition of Done (DoD) define os critérios que **toda** história de usuário precisa cumprir para ser considerada concluída. Uma história só é marcada como "Done" quando atende a **todos** os itens desta lista.

Esta DoD foi construída a partir da [Visão da Empresa](visao.md): um site onde clientes e pacientes entram em contato e são direcionados ao profissional certo (médicos e profissionais de educação física), com links de contato por área especializada.

---

## Critérios gerais

### Funcionalidade

- [ ] A funcionalidade foi implementada conforme descrita na história de usuário
- [ ] Todos os critérios de aceitação foram atendidos e verificados manualmente
- [ ] Casos de erro foram tratados (ex: campo vazio, dado inválido, falha de rede, link de contato quebrado)
- [ ] O fluxo funciona para os três públicos afetados pela história (funcionário, paciente, cliente), quando aplicável

### Qualidade de código

- [ ] O código passou por revisão de pelo menos um outro membro do grupo (code review via Pull Request)
- [ ] Não há código comentado, `console.log` ou dados de teste esquecidos no PR
- [ ] As variáveis e funções têm nomes descritivos em português ou inglês (sem mistura)

### Testes

- [ ] A funcionalidade foi testada manualmente no navegador (caminho feliz e principais erros)
- [ ] Pelo menos um teste automatizado cobre o caminho feliz da história
- [ ] Histórias de **contato com a empresa** e **direcionamento ao profissional** têm obrigatoriamente testes para os cenários de erro mais prováveis (ex: formulário incompleto, e-mail ou telefone inválido, nenhum profissional disponível na área escolhida)
- [ ] Nenhum teste existente foi quebrado pelo PR

### Experiência e acessibilidade

Como o público inclui pessoas com dificuldades físicas e mentais, a usabilidade faz parte do "pronto".

- [ ] A tela funciona bem no celular e no computador (layout responsivo)
- [ ] Textos legíveis, com bom contraste e botões grandes o suficiente para clicar ou tocar com facilidade
- [ ] A linguagem é simples e clara, sem termos técnicos desnecessários
- [ ] O usuário sempre sabe qual é o próximo passo (ex: mensagem de confirmação após enviar um pedido de contato)

### Privacidade e segurança

Pacientes compartilham informações pessoais e de saúde, então esses cuidados são obrigatórios.

- [ ] Dados pessoais coletados são apenas os necessários para a funcionalidade
- [ ] Nenhuma senha, chave de API ou dado pessoal real foi enviado ao repositório
- [ ] Dados sensíveis não aparecem em logs, URLs ou mensagens de erro

### Conteúdo dos profissionais e parceiros

Aplica-se a histórias que exibem profissionais, parceiros (prefeituras, academias) ou links de contato.

- [ ] Os links e contatos exibidos foram conferidos e funcionam
- [ ] Cada profissional aparece na área especializada correta
- [ ] As informações exibidas foram aprovadas pela pessoa responsável ou pelo profissional

### Integração

- [ ] O código está no branch principal após aprovação do Pull Request
- [ ] A funcionalidade funciona no ambiente de homologação (não apenas local)
- [ ] O Pull Request está vinculado à história de usuário no GitHub Projects

### Rastreabilidade

- [ ] O card da história no GitHub Projects foi movido para a coluna "Done"
- [ ] Os critérios de aceitação foram verificados e confirmados no card

---

## O que NÃO faz parte da DoD

- Performance otimizada além do básico (não é critério nesta fase)
- Documentação detalhada de código (não é exigida para este projeto)
- Testes automatizados para todos os cenários (apenas os críticos)
- Integração com sistemas externos de agendamento ou pagamento (fora da visão atual)

---

## Observação

A DoD se aplica a **todas as histórias**, independente do épico ou sprint. Se uma história cumpre os critérios de aceitação mas não passou por code review, ela **não está done**.
