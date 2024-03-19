# Guia de Estrutura do Projeto Frontend
Este projeto utiliza Next.js como framework principal para o desenvolvimento frontend de uma aplicação de gerenciamento financeiro. Além disso, são utilizadas as seguintes tecnologias e configurações:

- Biblioteca de UI: Material-UI para fornecer componentes estilizados e prontos para uso.
- Requisições HTTP: Axios ou fetch API para realizar requisições HTTP para o backend.
- Testes: Jest e React Testing Library para escrever e executar testes unitários e de integração.
- Linting: ESLint para manter um código limpo e consistente.
- Formulários: Formik para facilitar a criação e validação de formulários.
- Estilização: tailwind css ou sass.

## Configurações do Projeto:
- Dockerização da Aplicação: O projeto será dockerizado para facilitar a implantação e o gerenciamento de contêineres. O Docker será utilizado para criar imagens da aplicação frontend, permitindo a execução consistente em diferentes ambientes e simplificando o processo de implantação.
- Hooks de Pré-Commit: Utilização do Husky e lint-staged para automatizar tarefas antes de cada commit no repositório de código. Isso inclui a execução do ESLint para verificar e corrigir automaticamente problemas de estilo no código JavaScript, além da execução de testes para garantir a integridade das funcionalidades existentes.
- Considera utilizar commit lint
  
## Configuração do Repositório
- Crie um repositório Git para o projeto.
- Clone o repositório para o seu ambiente local.

## Estrutura do Projeto

```sh
project-root/
│
├── api/                    # Estrutura da API em Node.js
│   ├── routes/             # Definições das rotas da API
│   │   ├── index.js        # Arquivo principal de roteamento
│   │   └── ...             # Outros arquivos de rota
│   │
│   ├── controllers/        # Controladores da API
│   │   ├── index.js        # Arquivo principal de controladores
│   │   └── ...             # Outros arquivos de controlador
│   │
│   ├── models/             # Modelos de dados da API (opcional)
│   │   └── ...             # Definições de modelos de dados
│   │
│   └── middlewares/        # Middlewares da API (opcional)
│       └── ...             # Funções de middleware
│
├── modules/                # Módulos da aplicação (cada página é um módulo)
│   ├── dashboard/          # Módulo do dashboard
│   │   ├── components/     # Componentes específicos do dashboard
│   │   ├── context/        # Contexto específico do dashboard (se necessário)
│   │   ├── hooks/          # Hooks específicos do dashboard (se necessário)
│   │   ├── services/       # Serviços específicos do dashboard
│   │   ├── utils/          # Utilitários específicos do dashboard
│   │   ├── styles/         # Estilos específicos do dashboard
│   │   └── ...
│   │
│   ├── shared/             # Componentes, utils, context, hooks, etc. compartilhados
│   │   ├── components/     # Componentes compartilhados
│   │   ├── context/        # Contexto compartilhado (se necessário)
│   │   ├── hooks/          # Hooks compartilhados (se necessário)
│   │   ├── services/       # Serviços compartilhados
│   │   ├── utils/          # Utilitários compartilhados
│   │   ├── styles/         # Estilos compartilhados
│   │   └── ...
│   │
│   └── ...                 # Outros módulos da aplicação
│   │
│   ├── services/           # Lógica de negócio da API e chamadas externas
│   │   ├── index.js        # Arquivo principal de serviços
│   │   └── ...             # Outros arquivos de serviço
│
├── public/                 # Arquivos públicos (ícones, imagens, etc.)
│   └── ...
│
├── .gitignore              # Arquivos e diretórios ignorados pelo Git
├── Dockerfile              # Arquivo para construir a imagem Docker da aplicação
├── package.json            # Arquivo de configuração do npm com as dependências
├── README.md               # Documentação do projeto
└── ...
```


## Referências
- [NextJs](https://nextjs.org/docs)
- [ReactJs](https://react.dev/)
- [Eslint](https://eslint.org/docs/latest/)
- [Docker](https://docs.docker.com/)
- [Typescript](https://www.typescriptlang.org/docs/)
  