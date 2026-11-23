# Basic Full Stack: GraphQL + MySQL + Astro

A small school app built step by step to learn GraphQL from the ground up.

The app works with students, courses, instructors, classrooms, buildings and
departments. Data lives in a local MySQL database, a GraphQL server exposes it
as an API, and an Astro frontend displays it.

## What this project is for

This is a learning project, not a production app. Each part is kept as simple as possible so the GraphQL concepts stay easy to see:

- how a GraphQL **schema** describes data with **types** and **fields**
- how **queries** ask for exactly the data they need
- how **resolvers** connect the schema to a real MySQL database
- how **nested relationships** (student → course → classroom) work
- how **aliases**, **fragments**, **arguments** and **variables** make queries flexible
- how to test and explore an API with **Apollo Studio**, **GraphQL Network Inspector** and **GraphQL Voyager**

## Stack

| Layer | Technology |
|---|---|
| Database | MySQL 8 (local) with the University sample database |
| API | GraphQL server on Node.js |
| Frontend | Astro |

## Requirements

- **Node.js** 18 or newer (`node --version`)
- **npm** (comes with Node.js)
- **MySQL** 8 running locally (`mysql --version`)
- **Git**
- A browser, for Apollo Studio and the frontend

## Project structure

```
basic_full_stack/
├── database/   # how to set up the database, plus our own SQL
├── server/     # GraphQL server (in progress)
└── client/     # Astro frontend (planned)
```

## Getting started

1. Set up the database: see [database/README.md](database/README.md)
2. Server setup: *coming soon*
3. Frontend setup: *coming soon*
