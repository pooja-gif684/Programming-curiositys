# Python

Python is a general-purpose programming language known for readable syntax and a broad ecosystem.

## What you'll learn

- How Python code is commonly written and executed
- Where Python is frequently used
- How libraries extend what Python programs can do

## Explore further

Compare it with [JavaScript](javascript.md), [Java](java.md), and the [three-language overview](python-vs-javascript-vs-java.md).

## Curiosity Questions

81. Why is Python popular for AI?

   Python has readable syntax and a large ecosystem of mature scientific
   computing and machine-learning libraries. Many performance-intensive
   operations in those libraries run in optimized native code or on
   accelerators, so Python often coordinates the work rather than performing
   every numerical operation itself. Popularity does not mean Python alone
   makes an AI system fast or accurate.

87. Is Python actually slower than Java?

   For many CPU-bound tasks, conventional Python implementations such as
   CPython are slower than optimized Java because Java's just-in-time compiler
   can optimize frequently executed code and its type/runtime model differs.
   The result depends on the workload, implementation, libraries, and
   measurement; I/O-bound programs may spend most of their time waiting, and
   native libraries can change the comparison substantially.

89. Can Python call code written in C?

   Yes. Python can use C through extension modules and interoperability
   interfaces such as Python's C API, `ctypes`, or `cffi`. This is useful for
   reusing native libraries or speeding up specific work, but requires care
   with memory ownership, data types, build platforms, and errors.
