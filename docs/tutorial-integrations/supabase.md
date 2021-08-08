---
sidebar_position: 1
---

# PostgreSQL Database Hosted on Supabase

## Create Postgres Database with Supabase

Supabase includes a CLI for [local development](https://supabase.io/docs/guides/local-development).

```bash
npm install -g supabase
```

### Initialize Supabase project

```bash
supabase init
```

### Create table

```sql
CREATE TABLE databases_table (
  id bigint GENERATED BY DEFAULT AS IDENTITY PRIMARY KEY,
  inserted_at timestamp with time zone DEFAULT timezone('utc'::text, now()) NOT NULL,
  updated_at timestamp with time zone DEFAULT timezone('utc'::text, now()) NOT NULL,
  data jsonb,
  name text
);
```

```
Success. No rows returned
```

### Add `Name` column to table

```sql
ALTER TABLE databases_table
ADD COLUMN name text;
ADD COLUMN name text;
```

```sql
INSERT INTO databases_table(name, column2, …)
VALUES (value1, value2, …);
```