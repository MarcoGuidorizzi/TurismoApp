# 🗺️ TurismoApp

Sistema de gerenciamento de **Pontos Turísticos** com operações completas de cadastro, consulta, edição e remoção de informações.

> 🎥 Demonstração em vídeo em breve.

---

## 🛠️ Tecnologias Utilizadas

**Backend**

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Entity Framework Core](https://img.shields.io/badge/Entity_Framework_Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)

**Frontend**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## 🏗️ Arquitetura

O projeto foi desenvolvido utilizando o padrão **MVC (Model-View-Controller)**, separando as responsabilidades da aplicação em três camadas distintas.

```
Model → View → Controller
```

| Camada | Responsabilidade |
|---|---|
| **Model** | Define as entidades e regras de negócio da aplicação |
| **View** | Responsável pela interface visual apresentada ao usuário |
| **Controller** | Processa as requisições e coordena Model e View |

---

## 📁 Estrutura do Projeto

```
TurismoApp/
├── Controllers/
├── Models/
├── Views/
│   └── PontosTuristicos/
│       ├── Index.cshtml
│       └── Create.cshtml
├── wwwroot/
│   └── images/
│       └── logo.jpg
├── appsettings.json
└── TurismoApp.sln
```

---

## ✅ Funcionalidades

- 📋 Listagem de todos os pontos turísticos
- ➕ Cadastro de novo ponto turístico
- 🔍 Consulta de ponto turístico por ID
- ✏️ Edição de informações de um ponto turístico
- 🗑️ Remoção de ponto turístico

---

## ⚙️ Pré-requisitos

Antes de rodar o projeto, certifique-se de ter instalado:

- [.NET 10 SDK](https://dotnet.microsoft.com/download) — se não tiver .NET 10, altere o `TargetFramework` para `net8.0` no `TurismoApp.csproj`
- [Visual Studio Community 2022](https://visualstudio.microsoft.com/pt-br/vs/community/) com workload **"ASP.NET and web development"**
- [SQL Server](https://www.microsoft.com/pt-br/sql-server/sql-server-downloads) — SQL Server Express 2019/2022 ou `(localdb)\MSSQLLocalDB`
- [SSMS](https://aka.ms/ssmsfullsetup) *(opcional, para gerenciar o banco)*

---

## 🔧 Configuração do Banco de Dados

Edite o arquivo `appsettings.json` e ajuste a chave `ConnectionStrings:DefaultConnection` com o seu servidor:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.\\SQLEXPRESS;Database=TurismoDB;Trusted_Connection=True;TrustServerCertificate=True;"
}
```

Exemplos de `Server` conforme seu ambiente:

| Ambiente | Exemplo |
|---|---|
| SQL Express padrão | `Server=.\SQLEXPRESS;` |
| LocalDB (Visual Studio) | `Server=(localdb)\MSSQLLocalDB;` |
| Instância nomeada | `Server=DESKTOP123\SQL2019;` |
| Remoto com porta | `Server=localhost,1433;` |
| Com usuário e senha | `User Id=sa;Password=SuaSenha;TrustServerCertificate=True;` |

> ✅ O banco de dados é criado automaticamente na primeira execução via `EnsureCreated`.

---

## 🚀 Como Rodar o Projeto

### Via CLI

1. Clone o repositório:
```bash
git clone https://github.com/MarcoGuidorizzi/TurismoApp.git
```

2. Acesse a pasta do projeto:
```bash
cd TurismoApp
```

3. Restaure as dependências e execute:
```bash
dotnet restore
dotnet build
dotnet run
```

4. Acesse no navegador:
- `https://localhost:7160/`
- `http://localhost:5085/`

Rotas principais:
- `PontosTuristicos/Index` — listagem
- `PontosTuristicos/Create` — cadastro

---

### Via Visual Studio Community

1. Abra o arquivo `TurismoApp.sln`
2. Defina `TurismoApp` como projeto de inicialização
3. Ajuste o `appsettings.json` com seu `Server`
4. Pressione `F5` (Debug) ou `Ctrl+F5` (sem debug)
5. Acesse `PontosTuristicos/Create` para começar a cadastrar

---

## 🖼️ Assets

- Coloque sua imagem de logo em `wwwroot/images/logo.jpg`
- As views utilizam o caminho `~/images/logo.jpg`
- Se usar `.png`, ajuste o nome nas views correspondentes

---

## 🔍 Troubleshooting

| Problema | Solução |
|---|---|
| Falha de conexão com o banco | Verifique `Server`, `Database` e as credenciais no `appsettings.json`. Teste via SSMS. |
| SDK não encontrado | Altere `TargetFramework` para `net8.0` no `TurismoApp.csproj` |
| Arquivos estáticos não carregam | O projeto usa `app.UseStaticFiles()`. Certifique-se de que os arquivos estão em `wwwroot` |

---

## 👨‍💻 Autor

Feito por **Marco Guidorizzi**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/marco-guidorizzi-314282219/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MarcoGuidorizzi)
