#Project Overview
Purpose
This project provides a RESTful API for managing stock information stored in a PostgreSQL database. It allows users to create, retrieve, update, and delete stock records.

Key Features
CRUD Operations: Supports Create, Read, Update, and Delete operations for stock data.
PostgreSQL Database: Uses PostgreSQL as the primary data storage.
RESTful API: Provides a standard RESTful interface for interacting with stock data.
Gorilla Mux Router: Uses Gorilla Mux for request routing and handling.
.env Configuration: Uses godotenv to manage environment variables, such as the database connection string.
Supported Platforms or Requirements
Go 1.16 or higher
PostgreSQL database
lib/pq PostgreSQL driver
github.com/gorilla/mux
github.com/joho/godotenv
Getting Started
Installation or Setup Instructions
Clone the repository:

git clone <repository_url>
Navigate to the project directory:

cd go-postgres-stocks-yt
Create a .env file: Create a .env file in the root directory with the following content, replacing the placeholder with your actual PostgreSQL connection string: POSTGRES_URL="postgres://user:password@host:port/database"

**Note:** Ensure your PostgreSQL server is running and accessible.
Install dependencies:

go mod download
go mod tidy
Run the application:

go run main.go
The server will start on port 8080.

Dependencies or Prerequisites
Go: Make sure Go is installed on your system. You can download it from the official Go website: https://golang.org/dl/
PostgreSQL: You need a running PostgreSQL database instance. You can download and install it from the official PostgreSQL website: https://www.postgresql.org/download/
Go Packages: The following Go packages are required and will be installed using go mod:
github.com/gorilla/mux
github.com/joho/godotenv
github.com/lib/pq
Code Structure
go-postgres-stocks-yt/ ├── middleware/ │ └── handlers.go # Contains the handler functions for API endpoints. ├── models/ │ └── models.go # Defines the data models (Stock). ├── router/ │ └── router.go # Configures the API routes using Gorilla Mux. ├── go.mod # Go module file for dependency management. ├── main.go # Entry point of the application.

Key Components
main.go: The main application file that initializes the router and starts the HTTP server.
router/router.go: Defines the API routes and associates them with the corresponding handler functions in the middleware package.
middleware/handlers.go: Contains the handler functions that implement the API logic, including database interactions.
models/models.go: Defines the Stock struct, which represents the data structure for stock information.
API Documentation
Endpoints
| Method | Endpoint | Description | Input (Request Body)
