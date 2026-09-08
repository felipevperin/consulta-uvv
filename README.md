# Sistema de Gestão de Consultas UVV

Aplicação Web em **ASP.NET Core MVC** com **Entity Framework Core (Code First)** para cadastro de usuários, login e gerenciamento de consultas.

## Integrantes do grupo
- (felipe vieira perin)
- (nome 2)
- (nome 3)
- (nome 4)

## Tecnologias
- C# / ASP.NET Core 8.0 (MVC)
- Entity Framework Core (Code First + Migrations)
- SQL Server
- Autenticação via Cookies (`[Authorize]`)

## Como configurar e rodar o projeto

### Pré-requisitos
- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- SQL Server (LocalDB, Express ou Docker)

### Passo a passo

1. Clone o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd SistemaConsultasUVV
   ```

2. Restaure os pacotes:
   ```bash
   dotnet restore
   ```

3. Ajuste a connection string em `appsettings.json` se necessário (por padrão usa o LocalDB):
   ```json
   "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=SistemaConsultasUVV;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True"
   ```

4. Crie a primeira Migration (caso ainda não exista):
   ```bash
   dotnet ef migrations add InitialCreate
   ```

5. Aplique a Migration no banco de dados:
   ```bash
   dotnet ef database update
   ```

6. Execute a aplicação:
   ```bash
   dotnet run
   ```

7. Acesse no navegador: `https://localhost:5001` (ou a porta exibida no terminal).

## Funcionalidades
- Cadastro de novos usuários (senha armazenada com hash, nunca em texto puro)
- Login e Logout via autenticação por Cookies
- CRUD completo de Consultas (criar, listar, editar, excluir) — acessível apenas a usuários autenticados
- Validação de dados no servidor com Data Annotations

## Vídeo demonstrativo
🔗 [Link do vídeo (https://youtu.be/_JvzMJxzJKQ) mostrando cadastro, login e registro de consulta](#)
