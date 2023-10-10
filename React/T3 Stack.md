### Stack:
Next.js
tRPC
TypeScript
```
#Sometimes you want to restart the ts server
CTRL SHIFT P (in VSCODE)
TypeScript: Restart TS server
```
Tailwind

### Deployed on:
- Clerk 
	- authentication (user  management)
	- [Dashboard | Clerk.com](https://dashboard.clerk.com/apps/app_2WQt7in0y7d0CSJgetCi63qcEAu/instances/ins_2WQt7hfObc7oCeJWCeg4ddOr6Gg?)
- Planetscale 
	- Advanced mysql platform
	- [chirpdb overview - PlanetScale](https://app.planetscale.com/yannick-lansink/chirpdb)
- Upstash
- Vercel
	- Hosting platform
- Axiom
	- Axiom's Vercel integration enables you to monitor the health and performance of your Vercel deployments
	- [vercel - Datasets - Axiom](https://app.axiom.co/weshowyou-lzts/datasets/vercel)

```
npm create t3-app@latest
```

```
npm run db:push
npm run dev
```

### Setup Prisma
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


Workflow for changes in database:
npx pisma db push
npm install # so typescript knows about the changes? (npx prisma generate)
```


### Setup Clerk
[Use Clerk with Next.js | Clerk](https://clerk.com/docs/quickstarts/nextjs)
```
npm install @clerk/nextjs

```
