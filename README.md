# End to end typesafety

[reference video](https://www.youtube.com/watch?v=ottWptFQJgk&list=PLn2e1F9Rfr6lKHqj3Ke8vlu_Ly92HhpuG&index=1) for project setup

## What is this?

The backend is a graphql-yoga server that uses prisma to connect to a postgres database.  The graphql schema was built with typescript and the types are generated from the schema.  This garuntees that the types are always in sync with the schema, and upon schema changes.  

For example, if a migration is made, and a type changes, a component on the frontend should be aware that this type has changed.  This is done by using the graphql-codegen tool to generate typescript types from the schema.  These types are then used in the frontend to ensure that the types are always in sync.
