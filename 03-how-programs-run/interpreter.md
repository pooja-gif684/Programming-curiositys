# Interpreter

An interpreter is a program that reads and executes instructions from another program, often through a runtime.

## What you'll learn

- How interpreted execution differs from ahead-of-time compilation
- Why many modern languages combine both approaches
- How a runtime can provide services beyond executing code

## Explore further

Learn how a running program is represented by an operating system in [processes](process.md).

## Curiosity Questions

36. How does Python read your `.py` file?

   Python opens the file, decodes its text, and parses it according to Python's
   grammar. It then executes the resulting program using its runtime; CPython
   normally compiles source to bytecode first and may cache that bytecode.

37. Does Python directly understand your source code?

   The Python implementation understands Python syntax, but the processor
   does not execute the source text directly. In CPython, source is parsed and
   compiled into bytecode, which the Python Virtual Machine evaluates; other
   Python implementations can use different techniques.

38. What is bytecode?

   Bytecode is a compact, lower-level instruction format used by a virtual
   machine or runtime. CPython bytecode is an implementation detail and is not
   the same as native processor machine code; its format can change between
   Python versions.

39. What is the Python Virtual Machine?

   The Python Virtual Machine is the runtime machinery that executes Python
   bytecode in implementations such as CPython. It handles operations such as
   evaluating expressions and calling functions, while relying on the
   operating system for processes, files, and other system services.
