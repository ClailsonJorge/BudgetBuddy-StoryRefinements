# Tela de Dashboard

## Contexto:
Nosso objetivo é criar a página de dashboard para uma aplicação de gerenciamento financeiro. Esta página será acessada apenas por usuários autenticados e permitirá o cadastro de gastos e receitas por mês e ano. Os usuários também poderão cadastrar transações de forma periódica, para que sejam replicadas nos meses seguintes. O time de produto espera uma página intuitiva e responsiva, que permita aos usuários registrar suas transações financeiras de forma eficiente. Eles desejam uma interface limpa e organizada, com campos claros para inserção de dados e botões de ação bem definidos.

### Validações (se necessário):

- Todos os campos (valor, categoria, data, etc.) devem ser preenchidos antes de serem enviados.
- Validação do formato da data para garantir que esteja no padrão correto (mês/ano).
- O valor da transação não pode ser negativo.
- Garantir que transações periódicas tenham intervalos de repetição válidos (por exemplo, diário, semanal, mensal).
  
> Observação: Todos os campos são obrigatórios.

## Comportamento
__Eu__ como usuário do BudgetBuddy

__Quero__ acessar a área logada de dashboard

__Para__ cadastrar meus gastos e receitas e assim ter controle das minhas finanças.

#### Tarefas de Frontend:

- Criar a interface do usuário para o formulário de cadastro de transações.
- Implementar validações de entrada de dados no frontend para garantir que os campos sejam preenchidos corretamente.
- Exibir feedback ao usuário após o envio do formulário (sucesso ou falha).
- Integrar com a API backend para enviar os dados do formulário e receber feedback.
- Criar interface para apresentar os dados ao usuário em duas colunas (Gastos e Receita)

#### Tarefas de Backend:
- Criar endpoints para lidar com o cadastro de gastos e receitas.
- Implementar lógica para lidar com transações periódicas e replicar os dados nos meses seguintes.
- Implementar validações nos dados recebidos do frontend.
- Integrar com o sistema de autenticação para garantir que apenas usuários autenticados tenham acesso à página.
  