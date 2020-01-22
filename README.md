# Project Setup

## Dependencies

### meta

`npm i -g meta`

**repos file**: [meta repos](./.meta)

### prisma

`sudo npm i -g --unsafe-perm prisma2`

## Setup repos

```console
meta git clone git@github.com:daaasbu/flag-core.git
cd flag-core
meta git pull
```

### Other helpful meta commands

`meta git status`  
`meta git checkout -b branch`  
`meta git commit -m file`  
`meta git push`

## Run Project

To run project with no setup: p
`npm run start:fresh`  
This will:

- npm install across all projects
- docker compose up postgres
- migrate the database to latest schema
- seed the database
- start the admin on http://localhost:3000
- start the graphql api on http://localhost:4000
- build the react client libray
- start an example Create React App on http://localhost:3000

## Run individual projects

Most of these commands are just pass throughs to their respective projects.

`npm run db`  
`npm run admin`  
`npm run build:client && npm run example`  
`npm run api`

### In Docker

This could use a little work still, don't have HMR working yet. So will require rebuilds for testing changes.

`sudo docker-compose up`

## Postgres

**To connect locally:**  
`psql - U postgres -h localhost`  
**password:** mypassword  
**connection string:** postgresql://postgres:mypassword@localhost?sslmode=prefer

### Run db standalone

`npm run db`  
or  
`sudo docker-compose up db`

### Migrate and Seed

This will migrate the schema and regenerate the graphql endpoints.  
`npm run generate`

This will seed the db with some sample records.  
`npm run seed`

## GraphQL

**Introspection server:**  
http://localhost:4000
