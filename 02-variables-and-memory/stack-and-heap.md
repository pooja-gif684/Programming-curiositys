# Stack and Heap

The stack and heap are common ways a runtime organizes memory for function calls and dynamically managed data.

## What you'll learn

- How function calls use stack frames
- Why dynamically sized data is often stored on the heap
- How language runtimes manage these regions

## Explore further

See [garbage collection](garbage-collection.md) for one way runtimes reclaim memory on the heap.

## Curiosity Questions

19. What happens to variables when a function finishes?

   The function's local scope stops being active when it returns. References
   held only by that scope can become unreachable, but objects still referenced
   elsewhere remain available; Python manages their memory rather than
   promising that it is freed at the instant the function ends.

26. What is a stack?

   A call stack tracks active function calls and their execution state, such
   as where to return after a call. A new frame is added as a function is
   called and removed as it returns. Runtime implementations differ in how
   they represent this state.

27. What is a heap?

   A heap is a region or allocation mechanism used for objects whose lifetimes
   are not simply tied to a function call. In Python, objects are managed by
   the runtime, which may allocate them on a heap; application code should not
   assume a particular physical layout.
