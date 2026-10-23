# Database Indexes

An index is an auxiliary data structure that helps a database find records without scanning every row.

## What you'll learn

- How indexes can speed up selected queries
- Why indexes consume storage and add write costs
- How to think about which fields might need an index

## Explore further

See [transactions](transactions.md) for another core database concept.

## Curiosity Questions

69. Why do we need indexes?

   Without a suitable index, a database may need to inspect many rows to find
   matching records. An index can make lookups, sorting, or joins faster, but
   consumes storage and must be updated on writes. Indexes should be selected
   based on actual queries and measured performance.
