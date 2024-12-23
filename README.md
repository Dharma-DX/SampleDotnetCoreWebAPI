.NET Core API with EF Core and JWT Authentication
This project is a simple .NET Core Web API that demonstrates the use of Entity Framework Core for data access and JSON Web Tokens (JWT) for authentication. The API includes basic CRUD operations for managing user data.

Features
Entity Framework Core: Used for database operations.
JWT Authentication: Secure the API endpoints with JWT tokens.
CRUD Operations: Create, Read, Update, and Delete operations for user entities.
CORS Support: Configured to allow cross-origin requests.
Technologies Used
.NET Core 6.0
Entity Framework Core
JWT Authentication
SQL Server
Getting Started
Prerequisites
.NET Core SDK
SQL Server
Installation
Clone the repository:

git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
Install the required NuGet packages:

dotnet restore
Update the database connection string in appsettings.json:

"ConnectionStrings": {
  "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=MyApiDb;Trusted_Connection=True;"
},
"Jwt": {
  "Key": "your_secret_key",
  "Issuer": "your_issuer",
  "Audience": "your_audience"
}
Run the migrations and update the database:

dotnet ef migrations add InitialCreate
dotnet ef database update
Run the application:

dotnet run
API Endpoints
POST /api/auth/login: Authenticate a user and return a JWT token.
GET /api/users: Retrieve all users.
GET /api/users/{id}: Retrieve a user by ID.
POST /api/users: Create a new user.
PUT /api/users/{id}: Update an existing user.
DELETE /api/users/{id}: Delete a user.
License
This project is licensed under the MIT License - see the LICENSE file for details.
