# 📌 Projeto: Web API Minimal com C# - CRUD de Pessoas

Este projeto é uma Web API desenvolvida em **C# utilizando .NET (Minimal API)**, que implementa um **CRUD (Create, Read, Update, Delete)** básico para gerenciar informações de pessoas. A API permite adicionar, listar, atualizar e excluir pessoas com armazenamento em um banco de dados SQLite.

---

## 🧱 Tecnologias Utilizadas

* [.NET 7 ou 8](https://dotnet.microsoft.com/)
* Minimal API (estilo enxuto de construção de APIs no .NET)
* [SQLite](https://www.sqlite.org/)
* [Entity Framework Core](https://learn.microsoft.com/ef/)
* EF Core Migrations

---


## 🧑‍💻 Funcionalidades da API

* 🔹 **Criar Pessoa**: `POST /person`
* 🔹 **Listar Todas as Pessoas**: `GET /person`
* 🔹 **Buscar Pessoa por ID**: `GET /person/{id}`
* 🔹 **Atualizar Pessoa**: `PUT /person/{id}`
* 🔹 **Excluir Pessoa**: `DELETE /person/{id}`

Cada pessoa contém os seguintes dados:

```json
{
  "id": "56c25eb7-404c-4e90-a16e-ecd5c9365177",
  "name": "João Silva"
}
```

---

## ⚙️ Configuração e Execução

### 1. Clone o repositório

```bash
git clone https://github.com/Isaac-Lima/CRUD-C-Sharp.git
cd CRUD-C-Sharp
```

### 2. Instale os pacotes necessários

```bash
dotnet restore
```

### 3. Crie o banco de dados com migrations

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

### 4. Execute o projeto

```bash
dotnet run
```

A API estará disponível em: `https://localhost:5001` ou `http://localhost:5000`

---

## 🧪 Testando a API

Você pode testar as rotas usando ferramentas como:

* [Postman](https://www.postman.com/)
* [Insomnia](https://insomnia.rest/)
* `curl` via terminal

Exemplo de requisição `POST` para criar uma nova pessoa:

```http
POST /pessoas
Content-Type: application/json

{
  "nome": "Maria Oliveira"
}
```

---

## 📌 Observações

* O projeto usa SQLite, um banco de dados leve e prático para testes e aplicações simples.
* É possível adaptar facilmente para outros bancos relacionais (como SQL Server ou PostgreSQL), modificando a connection string e o provedor do EF Core.
