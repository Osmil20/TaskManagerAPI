# DotNetTaskManager

API de gerenciamento de tarefas desenvolvida como desafio da **Trilha .NET da DIO**.  
Construída com **.NET 6**, **Entity Framework Core** e **SQL Server**.

![Swagger UI](./swagger.png)  
*Interface Swagger mostrando todos os endpoints implementados.*

![POST /Tarefa](./post-tarefa.png)  
*Exemplo de criação de tarefa via POST.*

![GET /Tarefa/ObterTodos](./get-obter-todos.png)  
*Exemplo de listagem de todas as tarefas.*

![DELETE /Tarefa/{id}](./delete-tarefa.png)  
*Exemplo de exclusão de uma tarefa.*

---

## Tecnologias Utilizadas

- C# / .NET 6
- Entity Framework Core 6
- SQL Server
- Swagger (Swashbuckle.AspNetCore)

---

## Funcionalidades

- Criar tarefas (POST /Tarefa)  
- Listar todas as tarefas (GET /Tarefa/ObterTodos)  
- Buscar tarefas por ID (GET /Tarefa/{id})  
- Buscar tarefas por título (GET /Tarefa/ObterPorTitulo)  
- Buscar tarefas por data (GET /Tarefa/ObterPorData)  
- Buscar tarefas por status (GET /Tarefa/ObterPorStatus)  
- Atualizar tarefas (PUT /Tarefa/{id})  
- Deletar tarefas (DELETE /Tarefa/{id})  

---

## Model de Tarefa

Exemplo de JSON:

json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}

Como Rodar o Projeto

1. Clone o repositório:

git clone https://github.com/SEU_USUARIO/DotNetTaskManager.git


2. Entre na pasta do projeto:

cd DotNetTaskManager


3. Configure a Connection String no appsettings.Development.json:

{
  "ConnectionStrings": {
    "ConexaoPadrao": "Server=localhost\\SQLEXPRESS;Database=DesafioTarefasDB;Trusted_Connection=True;"
  }
}


4. Atualize o banco de dados:

dotnet ef database update


5. Rode a aplicação:

dotnet run


6. Acesse o Swagger:

https://localhost:7295/swagger/index.html
