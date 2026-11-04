# 📚 Book Store

<p align="center">
  <strong>A .NET-Based Book Store Management Application</strong>
  <br />
  A layered application architecture with a dedicated Web API and data access components.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Language-C%23-512BD4?style=for-the-badge&logo=csharp&logoColor=white" alt="C Sharp" />
  <img src="https://img.shields.io/badge/Platform-.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/Architecture-Layered-2563EB?style=for-the-badge" alt="Layered Architecture" />
</p>

---

## 📖 Overview

**Book Store** is a C#/.NET application organized into multiple projects, separating the application interface, API, business objects, and data access responsibilities.

The solution follows a layered structure to keep application components organized and make the codebase easier to maintain and extend.

## ✨ Project Structure

The repository is organized into the following projects:

| Project | Responsibility |
|---|---|
| `BookStore` | Main application project |
| `BookStoreAPI` | API endpoints and HTTP communication |
| `BusinessObjects` | Business entities and data models |
| `DatAccess` | Data access implementation |
| `Repositories` | Repository layer for data operations |

## 🏗️ Architecture

```text
                 Client
                   |
                   v
          +------------------+
          |    BookStore     |
          | Main Application |
          +------------------+
                   |
                   v
          +------------------+
          |   BookStoreAPI   |
          |   API Layer      |
          +------------------+
                   |
                   v
          +------------------+
          |   Repositories   |
          | Repository Layer |
          +------------------+
                   |
                   v
          +------------------+
          |    DatAccess     |
          |  Data Access     |
          +------------------+
                   |
                   v
          +------------------+
          | BusinessObjects  |
          | Business Models  |
          +------------------+
```

*Conceptual architecture based on the repository's project organization.*

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| C# | Primary programming language |
| .NET | Application development platform |
| ASP.NET Core | API development (verify target framework in project files) |
| Visual Studio | Solution development and management |
| NuGet | Dependency management |

## 📁 Repository Structure

```text
book-store/
├── BookStore/           # Main application
├── BookStoreAPI/        # Web API project
├── BusinessObjects/     # Business entities and models
├── DatAccess/           # Data access layer
├── Repositories/        # Repository implementations
├── BookStore.sln        # Visual Studio solution
└── .gitignore
```

## 🚀 Getting Started

### Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/download)
- [Visual Studio](https://visualstudio.microsoft.com/) or [Visual Studio Code](https://code.visualstudio.com/)
- The database engine and configuration required by the application

### 1. Clone the Repository

```bash
git clone https://github.com/que-tran-gw/book-store.git
cd book-store
```

### 2. Restore Dependencies

```bash
dotnet restore BookStore.sln
```

### 3. Configure the Application

Review the project configuration files and update the required settings, such as:

- Database connection strings
- Application environment settings
- External service configuration, if applicable

Do not commit passwords, credentials, or other sensitive configuration values.

### 4. Build the Solution

```bash
dotnet build BookStore.sln
```

### 5. Run the Application

Open `BookStore.sln` in Visual Studio, set the appropriate startup project, and run the application.

Alternatively, run the API project from the command line:

```bash
dotnet run --project BookStoreAPI
```

The actual startup project and launch configuration may vary depending on the project settings.

## 🧪 Testing

Run the available test projects using:

```bash
dotnet test BookStore.sln
```

## 🔧 Development

The layered project structure helps separate responsibilities:

- Keep business entities and models in `BusinessObjects`.
- Implement data operations in `DatAccess`.
- Encapsulate data access through `Repositories`.
- Expose application functionality through `BookStoreAPI`.
- Keep the main application concerns within `BookStore`.

## 📌 Future Improvements

- Add comprehensive API documentation.
- Improve automated unit and integration test coverage.
- Add validation and centralized exception handling.
- Enhance application logging and monitoring.
- Document database schema and deployment procedures.

## 📄 License

No license information is currently specified in this repository.

---

<p align="center">
  Built with ❤️ using C# and .NET.
</p>
