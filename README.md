URL shortener built using Prisma + Node.js (PostgreSQL)

Features
- Define and migrate a `Book` model (id, title, description?, createdAt)
- Generate Prisma Client to a custom path (`generated/prisma`)
- Run database migrations and manage data with Prisma Studio
- Easy to integrate into a NestJS app or plain Node.js script

Tech stack
- Node.js 18+ as runtime
- Prisma 6.16.1 ORM and `@prisma/client` 6.16.1 for data access
- PostgreSQL (13+) as the database
- npm for scripts and dependency management

How to run this project
Navigate to your working directory, then

# Create project folder and initialize npm
mkdir nestjs-prisma
cd nestjs-prisma
npm init -y

# Install Prisma and client
npm install prisma --save-dev
npm install @prisma/client

# Initialize Prisma (creates prisma/ + .env + schema.prisma)
npx prisma init

# Configure environment (.env)
DATABASE_URL="postgresql://postgres:150104@localhost:5432/week2_db?schema=public"

# Run initial migration (creates tables in DB)
npx prisma migrate dev --name init

# (Optional) Open Prisma Studio to test CRUD
npx prisma studio

About
A minimal Prisma + PostgreSQL starter. Client is generated to `generated/prisma`, so import from there instead of `@prisma/client` unless you remove the custom output.

Resources
- Prisma docs: [Getting started](https://pris.ly/d/getting-started)
- Prisma Studio: [Studio guide](https://pris.ly/d/studio)


