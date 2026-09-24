# Job Listing App

A job listing application with a Spring Boot and MongoDB backend and a React frontend.

## Project Structure

- `SpringMongoDB-main` - Spring Boot REST API
- `UISpringMongodb-main` - React user interface

## Requirements

- Java 11 or newer
- Maven, or the included Maven wrapper
- Node.js and npm
- MongoDB

## Backend Setup

1. Configure the MongoDB connection in:

   `SpringMongoDB-main/src/main/resources/application.properties`

   Do not commit real database credentials. Use environment-specific configuration for shared repositories.

2. Start the backend:

   ```powershell
   cd SpringMongoDB-main
   .\mvnw.cmd spring-boot:run
   ```

   The API runs at `http://localhost:8080`.

## Frontend Setup

Open a second terminal and run:

```powershell
cd UISpringMongodb-main
npm install
npm start
```

Open `http://localhost:3000` in a browser.

## API Endpoints

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/allPosts` | Return all job posts |
| `GET` | `/posts/{text}` | Search job posts |
| `POST` | `/post` | Create a job post |
| `GET` | `/swagger-ui.html` | Open Swagger UI |

Example request:

```powershell
Invoke-RestMethod -Method Post -Uri http://localhost:8080/post -ContentType 'application/json' -Body '{"profile":"Java Developer","desc":"Spring Boot development","exp":2,"techs":["Java","Spring Boot","MongoDB"]}'
```

## Useful Commands

Backend tests:

```powershell
cd SpringMongoDB-main
.\mvnw.cmd test
```

Frontend production build:

```powershell
cd UISpringMongodb-main
npm run build
```

## Upload This Project to GitHub

Run these commands from the project root:

```powershell
git add .
git status
git commit -m "Add job listing application"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
git push -u origin main
```

Replace `YOUR_USERNAME` and `YOUR_REPOSITORY` with your GitHub username and repository name. If `origin` already exists, skip the `git remote add origin ...` command and run:

```powershell
git push -u origin main
```
