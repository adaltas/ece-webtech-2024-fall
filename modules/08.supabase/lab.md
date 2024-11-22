---
duration: 2h
---

# Lab: install and use Supabase

The Supabase platform helps developers in the creation of modern apps. Its core services include database, authentication, file storage, and auto-generated APIs.

## Objectives

- Supabase installation and integration
- PostgreSQL and row-level security

## Tasks

1. Supabase installation (medium level)
2. Create a `contacts` table (easy level)
3. Next.js integration (easy level)
4. Fetch data from Supabase (easy level)
5. Insert data into Supabase (medium level)
6. Row-level security (medium level)

## Part 1. Supabase installation (medium level)

Follow the official [self-hosting with Docker](https://supabase.com/docs/guides/hosting/docker) documentation.

The `supabase/docker` directory contains the necessary files to run Supabase locally. Copy this directory into your project root directory and call it `./supabase`.

To launch Supabase in development mode, run the following command:

```bash
docker compose -f ./docker-compose.yml -f ./dev/docker-compose.dev.yml up
```

That command will start the Supabase services and the Postgres database. The Supabase service will be available at `http://localhost:8000` and the Supabase Studio at <http://localhost:3000>.

Important: Make sure to never commit your `.env` files. They contain sensible information.

## Part 2. Create a `contacts` table (easy level)

From the [Supabase Studio](http://localhost:3001), go to the table editor and click on the "New Table" button. The table properties are:

- Name: `contacts`
- Description: `Contact form`
- Columns:
  | Name       | Type        | Default value | Primary | Options  |
  |------------|-------------|---------------|---------|----------|
  | id         | int8        |               | true    | identity |
  | created_at | timestamptz | now()         |         | nullable |
  | firstname  | text        |               |         | nullable |
  | lastname   | text        |               |         | nullable |
  | email      | text        |               |         |          |
  | message    | text        |               |         |          |

Go to the SQL Editor and insert a record into the `contacts` table:

```sql
INSERT INTO contacts (firstname, lastname, email, message) VALUES
  ('david', 'worms', 'david@adaltas.com', E'# Hello\nHope you are enjoying the course.');
```

Write a `select` query to return all the records stored inside the `contacts` table.

## Part 3. Next.js integration (easy level)

Follow the official [Supabase Next.js guide](https://supabase.com/docs/guides/with-nextjs).

Find the `API_EXTERNAL_URL` and `ANON_KEY` API Keys from `./supabase/.env`, and save them in environment variables in the `./app/.env` file (both `.env` and `env.local` are interpreted, I prefer `.env`) to expose them to the browser for you Next.js application (read more [here](https://nextjs.org/docs/basic-features/environment-variables#exposing-environment-variables-to-the-browser)):

   ```bash
   NEXT_PUBLIC_SUPABASE_URL=http://localhost:8000
   NEXT_PUBLIC_SUPABASE_ANON_KEY=XXXXXXXXXXXXX
   ```

## Part 4. Fetch data from Supabase (easy level)

Implement a REST API query to fetch a record from the database:

- Fetch a list of element from the `contacts` table and display them on your website.
- Fetch a single element from the `contacts` table and display it on its own page.

## Part 5. Insert data into Supabase (medium level)

Implement a REST API query to insert records into the database:

- Let users fill a form to insert a new record into the `contacts` table.

## Part 6. Row-level security (medium level)

From the Supabase SQL editor, activate row-level security on the `contacts` table. There is a button dedicated to this action on the top right side of the page.

Create a policy that allows anonymous users to insert `contacts` records and which forbids anonymous users to read those inserted records.

Check that anonymous can submit new contact information from `./pages/contact.js`.

Also, confirm that no record is displayed in `./pages/admin/contacts.js`. Disabling row-level security show display the records once again.
