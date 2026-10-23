# Hashing

A cryptographic hash function maps input data to a fixed-size digest in a way designed to be difficult to reverse.

## What you'll learn

- How hashes differ from encryption
- Why password storage uses specialized password-hashing functions
- What salts contribute to password protection

## Explore further

Compare with [encryption](encryption.md), which is designed to be reversible with a key.

## Curiosity Questions

75. What is hashing?

   A cryptographic hash function maps input of arbitrary length to a
   fixed-length digest. It is designed to be one-way and to make it difficult
   to find two inputs with the same digest, though hashes are not encryption
   and collisions are theoretically possible. For passwords, use a
   salted, deliberately slow password-hashing algorithm rather than a fast
   general-purpose hash such as plain SHA-256.
