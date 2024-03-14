# Tela de change Password

## Contexto:
A plataforma BudgetBuddy está em construção e esta deve ter uma página exclusiva para atualizar senha quando solicitado na página de forgot password. O usuário recebe um link no e-mail ao utilizar a página de forgot password, esse link contém um token como query params que servirá para validar a troca de senha com o servidor. O time de produto informou que para a atualização da senha do usuário, será necessário 2 campos um de novo password e um de confiorm password, o usuário deve receber feedbacks sobre erros de formulários e de requisições, seguem as validações:

### Novo password:
- Deve seguir a mesma regra do cadastro de senha
- No mínimo 8 dígitos
- Ao menos uma letra maíscula e uma minúscula
- Deve ter ao menos 1 número
- Deve ter ao menos 1 caractere especial
  
#### Password: 
- Deve ser igual ao password

> Observação: Todos os campos são obrigatórios.

## Comportamento
__Eu__ como usuário de BudgetBuddy

__Quero__  atualizar minha senha

__Para__ ter novamente acesso a área logada ou mesmo para renova-la.

#### Tarefas de Frontend:

- Criar a interface da página de alteração de senha, incluindo os campos para novo password, confirm password e botão de envio.
- Validar os campos do formulário do lado do cliente, exibindo mensagens de erro se os critérios de validação não forem atendidos.
- Enviar uma solicitação para o servidor com os dados do formulário ao enviar o formulário.
- Exibir feedback para o usuário com base na resposta do servidor, informando se a senha foi atualizada com sucesso ou se ocorreu algum erro.

#### Tarefas de Backend:

- Criar uma rota no servidor para lidar com a solicitação de atualização de senha, que aceite o token como parâmetro de consulta.
- Validar o token recebido na solicitação para garantir sua autenticidade e verificar se ele está dentro do prazo de validade.
- Implementar a lógica para atualizar a senha do usuário no banco de dados.
- Adicionar validações para os campos de novo password e confirm password, incluindo o mínimo de 8 caracteres, pelo menos uma letra maiúscula e minúscula, pelo menos um número e pelo menos um caractere especial.
- Responder à solicitação com feedback sobre o sucesso ou falha da atualização da senha.