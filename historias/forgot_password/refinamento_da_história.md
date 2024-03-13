# Tela de Forgot Password

## Contexto:
A plataforma BudgetBuddy está em construção e esta deve ter uma página exclusiva para solicitar o reset da senha, assim, estes usuários poderão recuperar a senha caso esta seja perdida ou esquecida. O time de produto informou que para o reset da senha do usuário, será necessário o e-mail da conta cadastrada. Ao entrar com o e-mail e submeter o formulário o usuário deve receber uma mensagem de feedback caso ocorra sucesso ou não, casos possíveis:

### Após submeter o formulário
#### Caso o usuário tenha e-mail cadastrado
- será enviado para o e-mail do usuário o acesso a página de trocar senha, onde será enviado o token de validção
- o token deve expirar em 24 horas caso o usuário não troque a senha
- Na tela o usuário recebe uma mensagem de "Enviamos um link para seu e-mail!"
#### Caso o usuário tenha não e-mail cadastrado
- Não deverá enviar e-mail algum
- Na tela o usuário recebe uma mensagem de "Enviamos um link para seu e-mail!" (Para que o usuário não tenha a oção de checar se um e-mail está cadastrado) 

### Validação de campo
#### Email: 

- O e-mail deve ter um formato válido, ou seja, deve conter um símbolo "@" seguido de um domínio válido (por exemplo, exemplo@dominio.com);
- Deve ter um máximo de 100 caracteres;

> Observação: Todos os campos são obrigatórios.

## Comportamento
__Eu__ como usuário do BudgetBuddy

__Quero__  resetar minha senha

__Para__ atualiza-la em caso de esquecimento.

#### Tarefas de Frontend:

- Criar uma página de solicitação de reset de senha.
- Implementar um formulário para capturar o e-mail do usuário.
- Validar o campo de e-mail conforme as regras especificadas (formato de e-mail, comprimento máximo).
- Exibir mensagens de erro para feedback ao usuário caso as validações não sejam atendidas.
- Exibir uma mensagem de feedback após o envio do formulário, indicando se o e-mail foi enviado com sucesso ou se ocorreu algum erro.
- Implementar a lógica para enviar o e-mail do usuário para o servidor.
- Tratar as respostas do servidor (por exemplo, confirmação de envio de e-mail ou erro) e fornecer feedback adequado ao usuário.

#### Tarefas de Backend:

##### Geração e Envio de E-mail:

- Criar um serviço para gerar um token de validação e enviar um e-mail para o usuário com um link para a página de troca de senha.
- Gerenciar a expiração do token (por exemplo, definir uma validade de 24 horas).
- Enviar o e-mail apenas se o usuário fornecido estiver cadastrado no sistema.
  
##### Validação de E-mail:

- Verificar se o e-mail fornecido pelo usuário é válido.
- Verificar se o e-mail está registrado no sistema.
- Caso o e-mail não esteja cadastrado, retornar uma resposta especial para evitar a divulgação de informações confidenciais.

##### Segurança:

- Garantir que o token de validação seja seguro e não seja facilmente previsível.
  
##### Endpoint de Troca de Senha:

- Implementar a lógica para validar o token de validação e permitir que o usuário troque a senha.