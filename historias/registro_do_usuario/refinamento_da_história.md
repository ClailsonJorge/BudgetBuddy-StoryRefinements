# Tela de Cadastro

## Contexto:
A plataforma BudgetBuddy está em construção e esta deve ter uma página exclusiva para registrar seus usuário, assim, estes usuários cadastrados terão acesso a área de usuário logado da plataforma, para registro do usuário a equipe de produto viu a necessidade de registrar 3 informações cruciais além do password, com as seguintes premissas:

#### Nome: 
Usuário deve registrar esse campo para ser utilizado como identificador na plataforma, sendo assim, seguimos as seguintes validações:

- Deve ter ao menos 1 palavra;
- Deve ter entre 3 a 40 caracteres;
- Não deve permitir espaço em branco subsequente.

#### Email: 
Usuário deve registrar esse campo para ser utilizado como meio de comunicação e identificação forte e deve seguir as seguintes validações.

- O e-mail deve ter um formato válido, ou seja, deve conter um símbolo "@" seguido de um domínio válido (por exemplo, exemplo@dominio.com).;
- Deve ter um máximo de 100 caracteres;

#### Idade: 
Usuário deve registrar esse campo para ser utilizado como um dado estatístico, saber as faixas etárias que utilizam este campo, segue as seguintes validações:

- Formato de data: dd/mm/aaaa;

> Observação: Todos os campos são obrigatórios.

## Comportamento
__Eu__ como usuário do BudgetBuddy

__Quero__  acessar a página de cadastro

__Para__ registrar meu usuário na plataforma, para ter acesso a área de usuário logado.

#### Tarefas de Backend:

- Configurar route e controoler para lidar com as requisições de registro de usuários.
- Implementar lógica de validação para os campos de nome, e-mail e idade.
- Criar modelos de dados para armazenar informações de usuários, incluindo nome, e-mail e  idade, alinhando com time de frontend.
- Implementar lógica para verificar se o e-mail fornecido já está em uso por outro usuário.
- Configurar um sistema de armazenamento seguro para senhas de usuários.
- Implementar funcionalidade para persistir os dados do usuário.

#### Tarefas de Frontend:

- Criar a página de registro de usuários com formulário para inserção de nome, e-mail e idade.
- Desenvolver lógica de validação do formulário;
- Implementar feedback visual para indicar erros de validação no formulário, como mensagens de erro dinâmicas.
- Desenvolver componentes de sucesso e falha para exibir dar um feedback ao usuário após o seu registro.
- Testar a integração entre o frontend e o backend para garantir que os dados sejam enviados e recebidos corretamente.
- Redirecionar o usuário para a área de usuário logado após o registro bem-sucedido.
