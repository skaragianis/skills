---
name: pg-migration
description: Use when user wants to write database migrations in Postgres.
---

- table names are always plural eg. customers, not customer
- UUID id columns must be declared `id UUID PRIMARY KEY DEFAULT gen_random_uuid()`
- the database timezone must be set to be UTC
- always use TIMESTAMPZ, not TIMESTAMP
- include created_at and updated_at columns
- create separate migration files for each table, or dependent group if they must be created together
