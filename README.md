# db-migrate-study
Repo to practice db migration using go migrate



Level 1: Basic Table Creation
Scenario:
      Create a users table with:

      id (UUID, primary key)

      name (VARCHAR)

      email (VARCHAR, unique)

      Goal:

      Write a simple changelog.xml

      Run Liquibase using Go (os/exec)

      Learn basic Liquibase setup

✅ Level 2: Alter Table and Add Constraints
Scenario:
      Modify the users table:

      Add a created_at column with default now()

      Add a check constraint ensuring email contains '@'

      Goal:

      Demonstrate column modification

      Use constraints and safe evolution patterns

      Version changelogs correctly

✅ Level 3: Insert Seed Data
      Scenario:
      Seed initial users:
      [
        { "id": "uuid-1", "name": "Alice", "email": "alice@example.com" },
        { "id": "uuid-2", "name": "Bob", "email": "bob@example.com" }
      ]
      Goal:

      Practice <insert> tags


✅ Level 4: Add Relationships
        Scenario:
        Create a posts table with:

        id (UUID, primary key)

        user_id (UUID, foreign key to users)

        title (VARCHAR)

        body (TEXT)

        Goal:

        Create foreign key relationships

        Demonstrate multiple changelogs

        Maintain referential integrity

✅ Level 5: Rollback Strategy
        Scenario:
        Add rollback clauses for all previous changesets.

        Goal:

        Use <rollback> tags

        Learn to reverse schema changes

Level 6: Run Migration Using Makefile
Scenario:
You want to standardize the way developers and CI/CD pipelines run database migrations. Instead of running Liquibase via Go code, use a Makefile to encapsulate commands.
