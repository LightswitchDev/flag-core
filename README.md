# Project Setup
## Dependencies
### meta
`npm i -g meta`
## prisma
`sudo npm i -g --unsafe-perm prisma2`
## Setup repos
```console
meta git clone git@github.com:daaasbu/flag-core.git
cd flag-core
meta git pull
```

## Run Project
`sudo docker-compose up`

### Postgres
**To connect locally:**  
`psql - U postgres -h localhost`  
**password:** mypassword  
**connection string:** postgresql://postgres:mypassword@localhost?sslmode=prefer 
