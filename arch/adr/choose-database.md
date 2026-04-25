# Choosing a Database

## Status

Initial ADR

## Context

The application must store various types of objects. It must have a table for current items in the user's inventory and their expiration dates. It must also effectively store recipes, their text, and images. They must also be searchable and easily formatted for an LLM to use. The database must also store miscellaneous account data but will likely not store login data or financial data as third parties will be used for those.

## Decision

I am deciding between PostgreSql and MongoDB. For starters, I have briefly used both and am aware they are 2 very popular solutions. From my understanding, my decision will be based on how strict I want to build my database schemas. I am choosing PostgreSql so that I can plan out the schemas effectively and have strict data types. This may make it easier to interact with user entered data once it's in the database

## Consequences

Database Schemas and structure need to be determined.
