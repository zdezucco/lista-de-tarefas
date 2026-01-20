# 📝 Lista de Tarefas do Zucco | Zucco's Task List

---

## 🇧🇷 Português

### 📌 Descrição do Projeto
O **Lista de Tarefas do Zucco** é uma aplicação web desenvolvida para o gerenciamento de tarefas, permitindo que o usuário adicione, visualize, marque como concluídas e exclua tarefas de forma simples e intuitiva.

O usuário pode inserir o nome da tarefa em um campo de texto e adicioná-la ao sistema por meio do botão **ADICIONAR**. Antes da criação, é possível marcar a opção **"Está concluída?"**, fazendo com que a tarefa já seja registrada como concluída.  
Após adicionada, a tarefa é exibida em uma tabela, onde pode ser atualizada (marcada como concluída) ou removida.

---

### 🎯 Motivação e Justificativa
Este projeto foi desenvolvido durante as aulas da faculdade com o objetivo de **exercitar e consolidar os conhecimentos adquiridos** em desenvolvimento web e back-end.

A proposta do projeto é simular um cenário real de desenvolvimento de software, integrando uma interface web com uma API REST e um banco de dados relacional, aplicando conceitos fundamentais de arquitetura e organização de código.

---

### 🛠️ Tecnologias Utilizadas
- **HTML, CSS e JavaScript** — Construção da interface e interações do usuário;
- **Java com Spring Boot** — Desenvolvimento da API REST e gerenciamento das requisições HTTP;
- **Lombok** — Redução de código repetitivo e aumento da produtividade;
- **PostgreSQL** — Persistência e gerenciamento dos dados das tarefas.

---

### 🗂️ Estrutura do Projeto

#### 📁 `listadetarefasdozucco`
Pasta principal do projeto, responsável por conter toda a lógica da aplicação.

##### 📁 `controller`
Contém o arquivo `ControladorTarefa`, que atua como controlador Spring Boot da aplicação.  
É responsável por manipular as requisições HTTP relacionadas às operações CRUD, delegando a lógica de negócio ao serviço.

Principais responsabilidades:
- Salvar uma nova tarefa;
- Atualizar uma tarefa existente;
- Buscar uma tarefa por ID;
- Listar todas as tarefas;
- Excluir uma tarefa.

##### 📁 `model`
Contém a classe `Tarefa`, que representa o modelo de dados da entidade **Tarefa**.  
Essa classe é mapeada para uma tabela no banco de dados utilizando JPA.

- Define a estrutura da tabela `Tarefa`;
- Utiliza Lombok para gerar getters e setters automaticamente;
- Possui geração automática de ID gerenciada pelo banco de dados;
- Serve como base para criação e persistência das tarefas.

##### 📁 `repository`
Contém o arquivo `RepositorioTarefa`, responsável pela comunicação direta com o banco de dados.  
Estende a interface `CrudRepository` do Spring Data, fornecendo métodos prontos para operações CRUD.

##### 📁 `service`
Contém a classe `TarefaService`, que concentra a lógica de negócio da aplicação.  
É responsável por intermediar as operações entre o controller e o repositório, como:
- Salvar;
- Buscar por ID;
- Listar;
- Excluir tarefas.

##### 📄 `listadetarefasApp`
Arquivo principal da aplicação, responsável por iniciar o sistema.  
É identificado pela anotação `@SpringBootApplication`, que carrega toda a configuração e inicia o Spring Boot.

---

#### 📁 `resources`

##### 📁 `static`
Contém o arquivo `index.html`, que representa todo o front-end da aplicação.

- Utiliza CSS para estilização (cores, espaçamento, layout);
- Contém botões, inputs, tabela e demais elementos visuais;
- Inclui o JavaScript responsável pela interação com a API.

Funções JavaScript principais:
- `adicionarTarefa()` — Cria uma nova tarefa;
- `atualizarTabelaTarefas()` — Atualiza a tabela chamando a API;
- `marcarTarefaComoConcluida()` — Marca uma tarefa como concluída;
- `excluirTarefa()` — Exclui uma tarefa;
- `criarBotaoExcluir()` — Cria o botão de exclusão para cada tarefa;
- `atualizarTabelaTarefas()` — Atualiza a tabela ao carregar a página.

##### 📄 `application.properties`
Arquivo de configuração da aplicação, contendo as informações de conexão com o banco de dados PostgreSQL.

---

### ✅ Considerações Finais
A escolha de uma lista de tarefas como tema do projeto se deve à sua simplicidade conceitual aliada à aplicação de operações fundamentais de um sistema, como **CRUD (Create, Read, Update e Delete)**.

O projeto contribui para o desenvolvimento da lógica de programação, organização de código, entendimento da arquitetura MVC e integração entre front-end, back-end e banco de dados em uma aplicação web moderna.

---

## 🇺🇸 English

### 📌 Project Description
**Zucco's Task List** is a web application developed for task management, allowing users to add, view, mark as completed, and delete tasks in a simple and intuitive way.

Users can enter a task name into a text field and add it using the **ADD** button. Before adding the task, they can check the **"Is it completed?"** option, which registers the task as completed immediately.  
Once added, the task appears in a table where it can be marked as completed or deleted.

---

### 🎯 Motivation and Purpose
This project was developed during college classes with the purpose of **practicing and consolidating acquired knowledge** in both web and back-end development.

The project simulates a real-world software development scenario by integrating a web interface with a REST API and a relational database, applying fundamental architectural concepts.

---

### 🛠️ Technologies Used
- **HTML, CSS, and JavaScript** — User interface and interactions;
- **Java with Spring Boot** — REST API development and HTTP request handling;
- **Lombok** — Reducing boilerplate code;
- **PostgreSQL** — Data persistence and task management.

---

### 🗂️ Project Structure
The project follows a layered architecture with clear separation of responsibilities, including controller, service, repository, model, and front-end layers, following MVC principles.

---

### ✅ Final Notes
Choosing a task list as the project theme allows the practical application of **CRUD (Create, Read, Update, Delete)** operations, enabling a complete understanding of data flow between front-end, back-end, and database layers.

This project strengthens programming logic, code organization, MVC architecture understanding, and full-stack development skills.
