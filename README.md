# pg-crud-node
Basic project to CRUD a table

## CRUD A TABLE

The aim of this project is to just implement a CRUD app over a `students` table

## How to run

```bash
# clone this repo and run
npm install

# Start the app in dev
npm run dev  ## This runs node --env-file=.env index.js
```

## Database SETUP

Must setup your DB before connection.

```sql
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  rut VARCHAR(12) UNIQUE
);
```

## Setup your connection

Once setup and run your DB server, you must configure you connection `Client` or `Poll`. 

```
# .env
DATABASE=<your database name>
USER=<your databae user>
PASS=<your database user password>
```


```nodejs
  // Use your data storend on .env

  database: process.env.DATABASE,
  user: process.env.USER,
  password: process.env.PASS,
```

## Dependencies

[pg](https://node-postgres.com/) node modules collection to made a postgresql interface
