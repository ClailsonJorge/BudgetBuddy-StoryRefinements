# Guia de Estrutura do Projeto Backend
Este guia tem como objetivo auxiliar os desenvolvedores na configuração e desenvolvimento do backend utilizando Java com Spring Boot.

## Configuração do Repositório
- Crie um repositório Git para o projeto.
- Clone o repositório para o seu ambiente local.

## Estrutura do Projeto

```sh
projeto-backend/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── exemplo/
│   │   │           └── backend/
│   │   │               ├── config/
│   │   │               ├── controller/
│   │   │               ├── dto/
│   │   │               ├── entity/
│   │   │               ├── exception/
│   │   │               ├── repository/
│   │   │               ├── service/
│   │   │               └── BackendApplication.java
│   │   ├── resources/
│   │   │   ├── application.properties
│   │   │   └── ...
│   │   └── ...
│   └── test/
│       └── java/
│           └── com/
│               └── exemplo/
│                   └── backend/
│                       ├── controller/
│                       ├── service/
│                       └── ...
└── ...
```

##  Componentes do Projeto
1. Configuração
Diretório config: Contém classes de configuração do Spring Boot, como configurações do banco de dados, segurança, etc.
2. Controllers
Diretório controller: Contém classes responsáveis por receber requisições HTTP e direcioná-las para os serviços apropriados.
3. DTOs (Data Transfer Objects)
Diretório dto: Contém classes que representam objetos de transferência de dados entre as camadas da aplicação.
4. Entidades
Diretório entity: Contém classes que representam entidades do banco de dados.
5. Exceções
Diretório exception: Contém classes para tratamento de exceções personalizadas.
6. Repositórios
Diretório repository: Contém interfaces que definem operações de acesso ao banco de dados.
7. Serviços
Diretório service: Contém classes que implementam a lógica de negócio da aplicação.

## Ferramentas Recomendadas
- Code Linting: Utilize o plugin Checkstyle para garantir a consistência do código e seguir padrões de codificação.
- Dockerização: Utilize o Docker para containerizar a aplicação, facilitando a implantação e distribuição.

## Configuração Adicional
- Configure o arquivo application.properties para as propriedades de configuração do Spring Boot, como a porta do servidor, configurações do banco de dados, etc.
- Utilize o arquivo dockerfile para definir as instruções para a criação da imagem Docker da aplicação.

## Referências
- [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/)
- [Checkstyle](https://checkstyle.sourceforge.io/)