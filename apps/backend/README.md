# Backend API - Todo Application

Backend API untuk Todo Application dengan Express, MongoDB, dan JWT Authentication.

## Setup

1. Copy `env.example.txt` ke `.env`
2. Fill in environment variables
3. Install dependencies: `pnpm install`
4. Run development server: `pnpm dev`

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Todos (Protected)
- `GET /api/todos` - Get all todos
- `POST /api/todos` - Create todo
- `GET /api/todos/:id` - Get todo by ID
- `PUT /api/todos/:id` - Update todo
- `DELETE /api/todos/:id` - Delete todo

### Health
- `GET /health` - Health check
- `GET /health-checks` - Detailed health check

## API Documentation

Swagger documentation available at: `/api-docs`

## Development

```bash
# Start development server
pnpm dev

# Run tests
pnpm test

# Run unit tests
pnpm test:unit

# Run integration tests
pnpm test:integration
```

## Deployment

Backend is deployed as serverless functions on Vercel.

See main README.md for deployment instructions.

