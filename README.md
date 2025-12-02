# CodeSmoker Test: .NET Core Web API (#12)

A test repository for the CodeSmoker test suite demonstrating a .NET 8 Minimal Web API.

## Project Structure

```
├── TodoApi/
│   ├── Program.cs              # Main application with endpoints
│   ├── TodoApi.csproj          # Project file
│   ├── appsettings.json        # Configuration
│   └── Properties/
│       └── launchSettings.json # Launch configuration
└── TodoApi.sln                 # Solution file
```

## Features

- **.NET 8 Minimal API**: Lightweight API with minimal boilerplate
- **Entity Framework Core**: In-memory database for development
- **Swagger/OpenAPI**: Auto-generated API documentation
- **TypedResults**: Type-safe response handling

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/todoitems` | Get all todo items |
| GET | `/todoitems/complete` | Get completed items |
| GET | `/todoitems/{id}` | Get item by ID |
| POST | `/todoitems` | Create a new item |
| PUT | `/todoitems/{id}` | Update an item |
| DELETE | `/todoitems/{id}` | Delete an item |

## Getting Started

### Prerequisites

- .NET 8.0 SDK

### Run the API

```bash
cd TodoApi
dotnet run
```

### Access Swagger UI

Open http://localhost:5000/swagger in your browser.

### Build

```bash
dotnet build
```

### Test API with curl

```bash
# Get all todos
curl http://localhost:5000/todoitems

# Create a todo
curl -X POST http://localhost:5000/todoitems \
  -H "Content-Type: application/json" \
  -d '{"name":"New Task","isComplete":false}'

# Update a todo
curl -X PUT http://localhost:5000/todoitems/1 \
  -H "Content-Type: application/json" \
  -d '{"name":"Updated Task","isComplete":true}'
```

## Documentation

Built using latest documentation from:
- [ASP.NET Core Documentation](https://learn.microsoft.com/aspnet/core) - Microsoft's official ASP.NET Core docs

---

*This is a CodeSmoker test repository*
