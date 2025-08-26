# Projeto Integrado: API de Lista de Tarefas

### Descrição do Projeto

Este é o backend do projeto de Lista de Tarefas, uma API REST construída com Java e Spring Boot. Ela atua como a única fonte de verdade para a aplicação, gerenciando as operações de CRUD (Criação, Leitura, Atualização e Deleção) das tarefas. A API é consumida por dois clientes front-end separados: uma aplicação web em Angular e uma aplicação desktop em JavaFX.

A arquitetura do projeto é baseada no padrão cliente-servidor, onde o backend é desacoplado dos clientes, permitindo que diferentes interfaces consumam a mesma fonte de dados.

### Arquitetura da Solução

-   **Backend (Este Repositório):**
    -   API REST construída com **Spring Boot**.
    -   Camada de acesso a dados com **Spring Data JPA**.
    -   Banco de dados em memória **H2** para desenvolvimento.

-   **Frontend Web (Repositório Separado):**
    -   Aplicação de página única (SPA) construída com **Angular**.
    -   Consome a API REST deste projeto para exibir e manipular as tarefas.
    -   [Link para o Repositório Web](https://github.com/RafaelSilvaGomes/lista-tarefas-web)

-   **Frontend Desktop (Repositório Separado):**
    -   Aplicação desktop nativa construída com **JavaFX**.
    -   Também consome a mesma API REST, demonstrando a versatilidade de uma arquitetura desacoplada.
    -   [Link para o Repositório Desktop](https://github.com/RafaelSilvaGomes/lista-tarefas-desktop)

### Tecnologias Utilizadas

-   **Java 21**
-   **Spring Boot** (Spring Web, Spring Data JPA, H2, Lombok)
-   **Maven**
-   **RESTful API**

### Como Executar o Projeto

Para testar a solução completa, é fundamental seguir a ordem correta de execução.

#### Passo 1: Iniciar o Backend (Esta API)

1.  Abra este projeto (`lista-tarefas-api`) em sua IDE (IntelliJ IDEA, VS Code, etc.).
2.  Garanta que o Java 21 está configurado para o projeto.
3.  Execute a classe principal `ListaTarefasApiApplication.java`.
4.  Confirme que o servidor Spring Boot iniciou corretamente no console da IDE.

A partir de agora, a API está acessível em `http://localhost:8080`.

#### Passo 2: Iniciar a Aplicação Web (Angular)

1.  Abra o projeto `lista-tarefas-web` em um novo terminal.
2.  Se for a primeira vez, instale as dependências:
    ```bash
    npm install
    ```
3.  Inicie o servidor de desenvolvimento:
    ```bash
    ng serve --open
    ```
4.  O navegador será aberto automaticamente em `http://localhost:4200` exibindo a aplicação web, que se conectará à API.

#### Passo 3: Iniciar a Aplicação Desktop (JavaFX)

1.  Abra o projeto `lista-tarefas-desktop` em uma nova janela de IDE (ou em outra aba).
2.  Garanta que o Java 17 está configurado para este projeto.
3.  Execute a classe principal `MainApp.java`.
4.  A janela da aplicação desktop será exibida, e ela se conectará à mesma API.

**Nota:** As alterações feitas em uma aplicação (ex: deletar uma tarefa no site Angular) só aparecerão na aplicação desktop após clicar no botão "Atualizar" ou após adicionar/deletar uma tarefa por ela mesma.

---
