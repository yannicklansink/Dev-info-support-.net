Next.js
tRPC
TypeScript
Tailwind
Prisma (DB)
```
# Put inside the schema.prisma.
# Also get the env variables setup.
datasource db {
  provider     = "mysql"
  url          = env("DATABASE_URL")
  relationMode = "prisma"
}

generator client {
  provider = "prisma-client-js"
}

npx prisma db push # This tells Prisma to take current state of things in schema to set that to the database, wherever that server is.
npx prisma studio
```

Deployed on:
- Clerk -> authentication (user  management)
	- [Dashboard | Clerk.com](https://dashboard.clerk.com/apps/app_2WQt7in0y7d0CSJgetCi63qcEAu/instances/ins_2WQt7hfObc7oCeJWCeg4ddOr6Gg?)
- Planetscale -> Advanced mysql platform
	- [chirpdb overview - PlanetScale](https://app.planetscale.com/yannick-lansink/chirpdb)
- Upstash
- Vercel
- Axiom

```
npm create t3-app@latest
```

```
npm run db:push
npm run dev
```
