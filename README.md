# Nest.JS API Restful  🧠

A RESTful API built with [NestJS](https://nestjs.com/), following best practices for scalable, modular, and secure backend applications. It includes authentication, integration with a database, and Docker support for easy deployment.

## 🚀 Features

- RESTful API endpoints
- User authentication with JWT
- PostgreSQL integration via TypeORM or Prisma
- Dockerized for containerized environments
- Request validation with `class-validator`
- Modular project structure

## 🛠️ Technologies

- [NestJS](https://nestjs.com/)
- [TypeScript](https://www.typescriptlang.org/)
- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [TypeORM](https://typeorm.io/) or [Prisma](https://www.prisma.io/) *(choose one)*
- [JWT Authentication](https://jwt.io/)
- [Docker](https://www.docker.com/)
- [Class Validator](https://github.com/typestack/class-validator)

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/petersonchiquetto/nestjs-api-rest.git
cd nestjs-api-rest

# Install dependencies
npm install
````

## ⚙️ Environment Configuration

Create a `.env` file in the root directory:

```env
PORT=3000
DATABASE_URL=postgres://username:password@localhost:5432/mydb
JWT_SECRET=mysecretkey
```

## ▶️ Running the app

### Development

```bash
npm run start:dev
```

### Production

```bash
npm run build
npm run start:prod
```

### With Docker

```bash
# Build and run the app
docker-compose up --build
```

Access the API at: `http://localhost:3000`

## 🧪 Testing

```bash
# Unit tests
npm run test

# Test coverage
npm run test:cov
```

## 📁 Project Structure

```
src/
├── auth/             # Authentication logic (JWT, guards)
├── user/             # User module, controller, service
├── database/         # Database connection and entities
├── common/           # Shared utilities, DTOs, pipes
├── app.module.ts     # Main module
└── main.ts           # App entry point
```

## 📚 API Endpoints

### Auth

| Method | Route          | Description        |
| ------ | -------------- | ------------------ |
| POST   | /auth/login    | User login         |
| POST   | /auth/register | Create new account |

### Users

| Method | Route       | Description       |
| ------ | ----------- | ----------------- |
| GET    | /users      | List all users    |
| GET    | /users/\:id | Get user by ID    |
| PUT    | /users/\:id | Update user by ID |
| DELETE | /users/\:id | Delete user by ID |

> All user-related routes are protected and require a valid JWT token.

## 🔐 Authentication

This project uses JWT for authentication. After login, include the token in the `Authorization` header of requests:

```http
Authorization: Bearer <your-token>
```

## 🐳 Docker

A `docker-compose.yml` file is included for easy setup. It runs the NestJS API and a PostgreSQL database.

```bash
docker-compose up --build
```

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

> Created with using NestJS by [@petersonchiquetto](https://github.com/petersonchiquetto)

