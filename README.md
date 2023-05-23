# Full Stack Airbnb Clone with Next.js

## Setup: Tailwind, Prisma, MongoDB, NextAuth

## User Creation - MongoDB + prisma

```bash
npm install -D prisma

npx prisma init
```

### Setup schema.prisma

```bash
npx prisma db push

npm install next-auth @prisma/client @next-auth/prisma-adapter
npm install bcrypt @types/bcrypt
```

### Setup mongodb

[https://cloud.mongodb.com](https://cloud.mongodb.com)

- Connect to Cluster > MongoDB for VS Code

### Creating so many new PrismaClient() issue

```typescript
import { PrismaClient } from '@prisma/client'

declare global {
  var prisma: PrismaClient | undefined
}

const client = globalThis.prisma || new PrismaClient()
if (process.env.NODE_ENV !== 'production') globalThis.prisma = client

export default client
```
