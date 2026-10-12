# Dice API

NestJS service for recording dice rolls in Azure Cosmos DB. Part of the Azure training monorepo.

Run commands from `nodejs-microservices/`:

```bash
npm ci
npm run build --workspace=dice-api
npm test --workspace=dice-api -- --runInBand
```

Configure the Cosmos endpoint and credentials in the hosting environment. See `src/db.service.ts` for the current environment variable names. Do not commit connection strings or account keys.

This package is training material; production use requires a real data store, authentication and tested error handling.
