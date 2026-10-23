# Variables

A variable is a named way to refer to a value that a program can use.

## What you'll learn

- How names are connected to values
- How assignment and reassignment work
- Why variables make programs easier to understand and change

## Explore further

Continue with [memory](memory.md) to learn how values are represented while a program runs.

## Curiosity Questions

11. What happens internally when you write `x = 10`?

   In Python, the integer value `10` is an object, and assignment binds the
   name `x` to that object in the current scope. It does not declare a fixed
   memory box as it might in some other languages; the exact implementation
   details belong to the Python runtime.

14. Is `x` actually the value `10`?

   Conceptually, `x` is a name that refers to the integer object whose value is
   `10`; the name and the object are not the same thing. This distinction is
   useful when another name refers to the same object or when a name is
   reassigned.

15. What happens when you write `x = 10` and then `x = 20`?

   The second assignment rebinds `x` to the integer object `20`. It does not
   change the integer `10`; if no name or other reference can reach that old
   object, the runtime may eventually reclaim it.

16. What happens to `10`?

   The integer object remains available as long as it is reachable or otherwise
   retained by the runtime. Once it is no longer needed, Python's memory
   management can reclaim its storage; exactly when depends on the
   implementation.

17. What happens when you write `a = b = c = 100`?

   Python evaluates the right-hand value and binds all three names to it.
   Assignment runs from right to left, so the names refer to the same object
   initially.

18. Are `a`, `b`, and `c` three copies of `100`?

   In Python, the names initially refer to the same integer object rather than
   creating three separately observable copies. Integers are immutable, so
   using or rebinding one name does not change the value seen through the
   others.

### Rabbit Hole

1. When I type `x = 10`, where exactly does `10` go? Follow the trail:
   Variable → Object → Memory → RAM → Process → OS.

   Python creates or reuses an integer object representing `10` and binds the
   name `x` to it. The object is represented in the memory of the Python
   process; while the program runs, the operating system maps that process's
   memory into physical memory as needed. A virtual address is not a permanent
   physical location: the OS and hardware manage that mapping, and Python
   usually hides it from application code.
