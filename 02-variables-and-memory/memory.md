# Memory

Memory is the computer's working space for data and instructions used by running programs.

## What you'll learn

- The difference between short-term working memory and persistent storage
- How programs use addresses and values
- Why memory is organized into regions

## Explore further

Compare the [stack and heap](stack-and-heap.md), two important regions used by many programs.

## Curiosity Questions

12. Where is `10` stored?

   In a running Python program, `10` is represented by an integer object in
   the process's memory. The operating system and hardware manage where that
   memory is backed physically; there is no single universal RAM address for
   the value.

13. Where is `x` stored?

   `x` is a name in a Python namespace, such as a local function scope or a
   module's global namespace. That namespace maps names to objects; the
   implementation decides how to represent it in the process's memory.

21. What is RAM actually doing while your program runs?

   RAM temporarily holds the instructions and data that active programs need
   to access. The processor reads and writes that data while executing
   instructions; the operating system allocates and manages each process's
   view of memory.

22. What is the difference between RAM and storage?

   RAM is fast working memory that normally loses its contents when power is
   removed. Storage, such as an SSD, retains files without power and is used
   for long-term data; programs and data are typically loaded into RAM when
   needed.

23. Where does a Python variable live?

   A Python variable is a name binding in a namespace, not necessarily a
   dedicated box containing the value. The namespace and referenced object are
   represented in the process's memory, with details depending on the Python
   implementation.

24. What is a memory address?

   An address identifies a location in a process's virtual memory. Programs
   use addresses indirectly to access data, while the operating system and
   memory-management hardware map virtual addresses to physical memory.

25. Why can’t we normally see memory addresses in Python?

   Python is designed to let most programs work with object references and
   names instead of raw addresses, which simplifies programming and supports
   memory management. Low-level interfaces can expose implementation details,
   but those details are not portable and are rarely needed for ordinary code.
