# Wines Stock Web API

## Tecnologías utilizadas:

- **C#**: Lenguaje de programación orientado a objetos (OOP) desarrollado por Microsoft.
- **ASP.NET Core**: Framework web para la creación y manejo de APIs.
- **Entity Framework**: ORM utilizado para mapear las entidades de la API con los recursos de la base de datos.
- **SQLite**: Sistema de gestión de base de datos no tradicional, autocontenido y ligero, ya que todo se gestiona en un único archivo.

## Solicitudes HTTP disponibles:

### 1. Registrar un nuevo vino

- **Método**: `POST`
- **URL**: `https://localhost:7186/api/WineStock/Wine`
- **Cuerpo (BODY)**:
  ```json
  {
    "name": "string",
    "variety": "string",
    "year": 0,
    "region": "string",
    "stock": 0
  }
  ```
- **Respuestas posibles**:
  - **201 Created**: Representación del recurso creado.
  - **400 Bad Request**: El nombre del vino ya existe (no se admiten duplicados) o el cuerpo de la solicitud es nulo.

### 2. Registrar un nuevo usuario

- **Método**: `POST`
- **URL**: `https://localhost:7186/api/WineStock/User`
- **Cuerpo (BODY)**:
  ```json
  {
    "username": "string",
    "password": "string"
  }
  ```
- **Respuestas posibles**:
  - **201 Created**: Representación del recurso creado.
  - **400 Bad Request**: El nombre de usuario ya existe (no se admiten duplicados) o el cuerpo de la solicitud es nulo.

### 3. Obtener el stock de todos los vinos

- **Método**: `GET`
- **URL**: `https://localhost:7186/api/WineStock/WineStock`
- **Respuestas posibles**:
  - **200 OK**: Devuelve un diccionario con la estructura `{ "WineName": StockQuantity }`.
