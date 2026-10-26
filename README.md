# API Biblioteca

API REST desenvolvida em Java com Spring Boot para gerenciar uma biblioteca digital ou sistema de cadastro de livros, usuários e operações básicas do acervo.

## Visão geral

Este projeto é uma base inicial de API em Spring Boot. Atualmente ele contém a estrutura mínima para iniciar a aplicação e configurar o projeto, pronta para receber controladores, modelos, serviços e regras de negócio do domínio da biblioteca.

## Tecnologias

- Java 25
- Spring Boot 4.1.2
- Spring Web MVC
- Maven
- Maven Wrapper

## Estrutura do projeto

```text
ApiBiblioteca/
├── .mvn/
│   └── wrapper/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── br/com/aula/biblioteca/
│   │   │       └── BibliotecaApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/
│           └── br/com/aula/biblioteca/
│               └── BibliotecaApplicationTests.java
├── .gitattributes
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
```

## Pré-requisitos

Antes de executar o projeto, verifique se você possui:

- JDK 25 instalado
- Git
- Terminal/PowerShell/Prompt de comando

## Clonando o projeto

```bash
git clone https://github.com/PabloEtec/ApiBiblioteca.git
cd ApiBiblioteca
```

## Executando a aplicação

### Opção 1: usando o Maven Wrapper (recomendado)

No Linux/macOS:

```bash
chmod +x mvnw
./mvnw spring-boot:run
```

No Windows:

```powershell
mvnw.cmd spring-boot:run
```

A aplicação iniciará e, por padrão, ficará disponível em:

```text
http://localhost:8080
```

### Opção 2: gerando um pacote executável

```bash
./mvnw clean package
```

Depois:

```bash
java -jar target/biblioteca-0.0.1-SNAPSHOT.jar
```

## Configuração

O arquivo `src/main/resources/application.properties` contém as configurações básicas da aplicação:

```properties
spring.application.name=biblioteca
```

Você pode adicionar aqui configurações como:

- porta da aplicação
- banco de dados
- conexão com MySQL/PostgreSQL
- logs
- segurança

## Como a API está organizada

No momento, a aplicação ainda está em fase inicial e contém apenas a classe principal:

- `BibliotecaApplication`: ponto de entrada da aplicação Spring Boot

A partir desta base, é possível criar os seguintes elementos:

- `Controller` para endpoints REST
- `Entity` para representar livros, usuários e empréstimos
- `Repository` para acesso ao banco de dados
- `Service` para regras de negócio
- `DTO` para transporte de dados

## Endpoints

Até o momento, não há rotas implementadas nesta versão inicial do projeto. O objetivo do repositório é servir como estrutura base para a criação dos endpoints da API de biblioteca.

Quando os controladores forem criados, os endpoints normalmente seguirão um padrão como:

```text
GET /livros
GET /livros/{id}
POST /livros
PUT /livros/{id}
DELETE /livros/{id}
```

## Testes

Para executar os testes do projeto:

```bash
./mvnw test
```

## Dicas de desenvolvimento

- Mantenha a estrutura em pacotes organizada por domínio
- Use `@RestController` para expor endpoints HTTP
- Separe regras de negócio em `Service`
- Centralize a configuração do projeto em `application.properties` ou `application.yml`
- Documente cada endpoint futuramente com descrições de uso e exemplos

## Contribuição

1. Faça um fork do projeto
2. Crie uma branch para sua funcionalidade
3. Faça o commit das alterações
4. Abra um Pull Request

## Licença

Este projeto não possui licença definida no momento.

## Observações

Este repositório está em estado inicial de desenvolvimento e deve ser evoluído com os modelos e endpoints específicos da biblioteca desejada.
