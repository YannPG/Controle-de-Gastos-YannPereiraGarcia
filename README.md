# 📊 Controle de Gastos

Aplicação web simples para controle de gastos pessoais, permitindo o cadastro, visualização, edição e exclusão de receitas e despesas.

O projeto foi desenvolvido como parte de uma atividade acadêmica, utilizando **Spring Boot** no backend e **HTML/CSS** no frontend
---

### ✨ Features

* **Create**: Adicionar novos lançamentos (receitas ou despesas).
* **Read**: Visualizar todos os lançamentos em uma lista ordenada por data.
* **Update**: Editar as informações de um lançamento existente.
* **Delete**: Remover um lançamento da lista.
* **Interface Reativa**: As operações de CRUD atualizam a lista de lançamentos instantaneamente.

---

### 🚀 Tecnologias Utilizadas

**Backend:**
* **Java 21**
* **Spring Boot**
* **Spring Data JPA**
* **Hibernate**
* **Maven**

**Frontend:**
* **HTML/CSS**

**Banco de Dados:**
* **Neon** (para produção)
* **H2 Database** (para testes e desenvolvimento local)

---

### ⚙️ Como Configurar e Executar Localmente

1.  **Clone o repositório:**
    ```bash
    git clone ...
    ```

2.  **Configuração do Banco de Dados:**
    O projeto está pré-configurado para rodar localmente com o **H2 Database** no perfil padrão. Isso significa que você pode executar a aplicação sem precisar de um banco de dados externo.

    * **Para usar o H2:** Basta executar o comando abaixo. O H2 criará um banco de dados em memória automaticamente.
    * **Para usar um PostgreSQL local:** Altere o arquivo `application.properties` com suas credenciais e URL do PostgreSQL local.

3.  **Execute a Aplicação:**
    Use o Maven para compilar e iniciar o projeto.
    ```bash
    mvn spring-boot:run
    ```

4.  **Acesse a Aplicação:**
    Abra seu navegador e acesse `http://localhost:8080`.

---

### 🌐 Ambiente de Produção (Render)

A aplicação foi projetada para ser implantada facilmente no **Render**, utilizando o banco de dados **Neon.tech**.

As variáveis de ambiente são usadas para a conexão em produção. Ao implantar no Render, você deve configurar as seguintes variáveis no painel da sua aplicação:

* **`SPRING_PROFILES_ACTIVE`**: `prod`
* **`DB_URL`**: `jdbc:postgresql://...` (sua URL do Neon)
* **`DB_USERNAME`**: `...` (seu usuário do Neon)
* **`DB_PASSWORD`**: `...` (sua senha do Neon)

O `SPRING_PROFILES_ACTIVE` com o valor `prod` garante que o Spring Boot ignore as configurações do H2 e use as credenciais do Neon.

---

### 🚀 Acessar a Aplicação

A aplicação está no ar em:

<a href="https://crud-controle-gastos-gvdev.onrender.com/" target="_blank">https://crud-controle-gastos-gvdev.onrender.com/</a>
