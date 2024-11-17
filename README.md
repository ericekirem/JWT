# JWT Authentication Example

This project demonstrates how to implement JWT (JSON Web Token) authentication in an ASP.NET Core application.

## Features

- User login with email and password.
- JWT token generation upon successful login.
- JWT token validation for protected routes.

## Requirements

- .NET 8.0 (or higher)
- Entity Framework Core
- In-memory database (for development)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/jwt-authentication-example.git
    cd jwt-authentication-example
    ```

2. Install the required packages:

    ```bash
    dotnet restore
    ```

3. Run the application:

    ```bash
    dotnet run
    ```

4. The API should now be running on `https://localhost:5001`.

## Endpoints

- `POST /api/auth/login`: Login with email and password to get a JWT token.
- `GET /api/protected`: Access this endpoint only with a valid JWT token.

## Configuration

In `appsettings.json`, configure your JWT settings:

```json
{
  "Jwt": {
    "Key": "YourSecretKeyHere",
    "Issuer": "YourIssuer",
    "Audience": "YourAudience"
  }
}
