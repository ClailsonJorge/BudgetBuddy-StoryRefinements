# Tela de Login

## Contexto:
A plataforma BudgetBuddy está em construção e esta deve ter uma página exclusiva para login onde seus usuário poderão acessar a área logada da aplicação, assim, estes usuários poderão aproveitar as funcionalidades reservadas. O time de produto informou que para o login do usuário será necessário o e-mail e a senha, lembrando que o usuário deve ter se cadastrado para realizar login, sendo assim foi pedido um link que redirecione o usuário para a tela de cadastro e outro link para a recuperção de senha, como de costume.

Os campos devem ter as seguintes validações:

#### Email: 

- O e-mail deve ter um formato válido, ou seja, deve conter um símbolo "@" seguido de um domínio válido (por exemplo, exemplo@dominio.com);
- Deve ter um máximo de 100 caracteres;

#### Password: 

- Deve seguir a mesma regra do cadastro de senha
- No mínimo 8 dígitos
- Ao menos uma letra maíscula e uma minúscula
- Deve ter ao menos 1 número
- Deve ter ao menos 1 caractere especial

> Observação: Todos os campos são obrigatórios.

## Comportamento
__Eu__ como usuário do BudgetBuddy

__Quero__  fazer o login na plataforma, com meu email e senha

__Para__ acessar a área logada.

#### Tarefas de Frontend:

- Criar a página de login com os campos de e-mail, senha e botões de login, cadastro e recuperação de senha.
- Implementar um formulário para capturar os dados de entrada do usuário (e-mail e senha).
- Validar os campos do formulário conforme as regras especificadas (formato de e-mail, comprimento máximo, regras de senha, etc.).
- Exibir mensagens de erro para feedback ao usuário caso as validações não sejam atendidas.
- Incluir links de redirecionamento para a tela de cadastro e recuperação de senha.
- Implementar a lógica para enviar os dados de login (e-mail e senha) para o servidor.
- Tratar as respostas do servidor (por exemplo, autenticação bem-sucedida ou falha de autenticação) e fornecer feedback adequado ao usuário.
- Implementar a lógica para o redirecionamento do usuário após o login bem-sucedido.
- Implementar endpoints para as funcionalidades de cadastro e recuperação de senha, conforme os links disponíveis na página de login.

#### Tarefas de Backend:

##### Lógica de Autenticação:

- Implementar a lógica de autenticação no servidor para verificar se o e-mail e a senha fornecidos pelo usuário correspondem a uma conta existente.
- Validar se o e-mail segue o formato correto (com "@" e um domínio válido).
- Verificar se o e-mail está registrado no sistema.
- Verificar se a senha atende aos critérios de complexidade especificados (comprimento mínimo, presença de maiúsculas, minúsculas, números e caracteres especiais).

##### Gestão de Sessões:

- Criar e gerenciar a sessão do usuário após uma autenticação bem-sucedida.
- Enviar respostas ao cliente indicando se o login foi bem-sucedido ou não.
 
##### Segurança:

- Garantir que todas as comunicações entre cliente e servidor sejam seguras (usando HTTPS).
- Garantir a criptografia de senhas e tokens.
