# Garbage Collection

Garbage collection is automatic memory management that reclaims objects a program can no longer use.

## What you'll learn

- How a runtime identifies reachable objects
- Why automatic cleanup can simplify application code
- What trade-offs garbage collection introduces

## Explore further

Review [memory](memory.md) and the [stack and heap](stack-and-heap.md) to understand where managed data lives.

## Curiosity Questions

20. Who cleans unused memory?

   The language runtime and its memory manager handle memory reclamation for
   many languages. Python implementations commonly combine reference counting
   with a cyclic garbage collector; other languages may use different
   collectors or require programmers to manage resources more explicitly.

28. What is garbage collection?

   Garbage collection is runtime-managed discovery and reclamation of objects
   that a program can no longer reach. It reduces the need for manual object
   deallocation, though it does not clean every kind of resource automatically
   (files and network connections should still be closed).

29. Why doesn’t unused memory remain forever?

   Runtimes reclaim unreachable objects so memory can be reused by the same
   process. Operating systems also reclaim a process's memory when it exits.
   Some runtimes keep freed memory available for future allocations instead
   of immediately returning it to the OS.

30. What happens when your program consumes too much memory?

   The system may slow down as it moves memory pages to storage, reject new
   allocations, or terminate the process if it cannot continue safely.
   Programs should bound caches and input sizes, release unneeded references,
   and investigate memory growth rather than assuming garbage collection can
   fix every leak.
