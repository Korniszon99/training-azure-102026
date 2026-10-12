# Azure / DevOps Training — October 2026

**Training material for deploying a small Node.js microservice application with GitHub Actions and Azure.**

NestJS · Express · Fastify · Vite · Docker · Cosmos DB · Azure · GitHub Actions

This repository combines organizer documentation, participant/archive templates and an example microservice application in `nodejs-microservices/`. Deployment workflow files are already present in `.github/workflows/`; their runtime credentials belong in GitHub/Azure configuration, not in source.

## Local example

```bash
git clone https://github.com/Korniszon99/training-azure-102026.git
cd training-azure-102026/nodejs-microservices
npm ci
docker compose up --build
```

In another terminal run `npm run start --workspace=website`. The website uses Vite; Docker exposes settings, dice and gateway APIs on ports 4001, 4002 and 4003. Services use in-memory mock storage without `DATABASE_CONNECTION_STRING`; persistence requires a configured Cosmos DB connection. Docker deployment is separate from the static frontend build.

## Verification

```bash
npm run build --workspace=dice-api
npm test --workspace=dice-api -- --runInBand
npm test --workspace=settings-api
npm run build --workspace=website
npm audit
npm audit --omit=dev
```

The updated dependency lock removes critical/high findings from the audited dependency tree. Remaining moderate findings in development tooling are recorded in [SECURITY.md](SECURITY.md); this does not imply a vulnerability-free application. The Fastify test command does not enforce a repository-wide coverage threshold.

## Training organization

- [participants/](participants/) — participant entries.
- [archive/](archive/) — final training artifacts.
- [organizer-checklist.md](organizer-checklist.md) — organizer checklist.
- [templates/PARTICIPANT.md](templates/PARTICIPANT.md) — entry template.
- [nodejs-microservices/](nodejs-microservices/) — application and upstream workshop material.

Participants can use repositories named `training-azure-102026-<github-login>` in their chosen organization and record the final deployment, workflow and lessons learned here.

## Attribution and production scope

The microservice example retains the upstream author's attribution and MIT license in `nodejs-microservices/`; it should not be presented as an entirely original architecture. The training contribution is the organization, integration and deployment exercises.

Mocks, demo identity handling and workshop defaults are not a production security model. Before reusing this stack, implement authentication/authorization, durable data storage, input validation, rate limits and a tested deployment configuration. This is a supporting DevOps/teaching project, not a lead CV/AI case study.
