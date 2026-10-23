# Database Transactions

A transaction groups database operations so they can be handled as a logical unit.

## What you'll learn

- The ACID properties and why they matter
- How commit and rollback affect changes
- Why transaction boundaries influence correctness

## Explore further

Learn about data models in [SQL](sql.md) and [NoSQL](nosql.md).

### Rabbit Hole

7. What happens if two users try to modify the same database record at exactly
   the same time?

   The database coordinates concurrent writes according to its isolation and
   locking or versioning rules. One update may wait, conflict, or overwrite
   another depending on the operation and design. Transactions, constraints,
   optimistic version checks, and suitable isolation levels help prevent lost
   updates and preserve consistency; applications should handle conflicts
   explicitly.
