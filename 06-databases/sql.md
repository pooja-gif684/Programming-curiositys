# SQL Databases

SQL databases organize data into related structures and provide a language for querying and changing that data.

## What you'll learn

- How tables, rows, and columns represent information
- How SQL retrieves and modifies data
- When relational structure is useful

## Explore further

Compare with [NoSQL databases](nosql.md) and learn about [indexes](indexes.md).

## Curiosity Questions

61. Why can’t we simply store everything in Python variables?

   Variables normally live only while a process is running, and their data is
   lost when it exits. Databases provide durable storage, querying, controlled
   concurrent access, and recovery mechanisms that are difficult to build
   reliably with in-memory variables alone.

62. Why do applications need databases?

   Databases store and organize information so it can be retrieved and changed
   across program runs and shared by users or services. They can enforce
   constraints and coordinate concurrent operations, helping an application
   maintain consistent records.

63. What happens when you click “Save”?

   The application validates the input and sends a write operation to its
   backend. The backend applies business rules and submits a database command;
   the database checks permissions and constraints, updates its data, and
   usually records enough information for recovery before confirming success.
   The application then reports the result to the user.

64. Where does the data physically go?

   A database may keep active data in RAM and persist it to storage devices
   such as SSDs, often through database files and transaction logs. A hosted
   database may replicate or back up data on other machines or locations.
   The exact physical layout depends on the database and its deployment.

65. What is a table?

   In a relational database, a table is a named structure that organizes
   records into rows with defined columns. Relationships between tables can
   be represented through keys.

66. What is a row?

   A row is one record in a relational table, containing a value for each
   column (or a permitted null value). For example, a user table might have
   one row for each user.

67. What is a column?

   A column defines one attribute of records in a relational table, such as
   `email` or `created_at`, and usually has a data type and optional rules.
   Choosing types and constraints helps keep stored data meaningful.

68. Why do we need primary keys?

   A primary key uniquely identifies each row so it can be retrieved or
   referenced reliably. A database enforces its uniqueness and non-null
   requirements; other tables can use foreign keys to refer to it.
