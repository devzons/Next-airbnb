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

### Github

`Settings > Developer settings > OAuth Apps > new OAuth app`

### Google developer console

- New Projects
- Project name: next-airbnb, create
- Select project
- APIs and services > Enable APIS and services
- OAuth consent screen > External
  - App name, User support email, Developer contact information, save and continue
  - Save and Continue
  - Save and Continue
- Credentials
  - Create credentials > OAuth client ID
  - Application type: Web application
  - Authorised redirect URIs: http://localhost:3000/api/auth/callback/google
  - Create

## World Countries, Map

```bash
npm install world-countries
npm install react-select

npm install leaflet @types/leaflet react-leaflet

```
