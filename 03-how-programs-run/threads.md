# Threads

A thread is a sequence of execution within a process; multiple threads can make progress within the same program.

## What you'll learn

- How threads share process resources
- Why concurrency can improve responsiveness
- Why coordinating shared data requires care

## Explore further

Start with [processes](process.md) to understand the environment threads run inside.

## Curiosity Questions

34. What is a thread?

   A thread is a path of execution scheduled by the operating system within a
   process. Threads in one process generally share its memory and open
   resources, which makes communication convenient but means shared data must
   be coordinated to avoid race conditions.
