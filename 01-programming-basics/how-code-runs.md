# How Code Runs

Code must be translated, interpreted, or otherwise prepared before a computer can carry out its instructions.

## What you'll learn

- The roles of source code, runtimes, and machine instructions
- Why running a program can involve several stages
- How a small change in code becomes an observable result

## Explore further

The [compiler](../03-how-programs-run/compiler.md) and [interpreter](../03-how-programs-run/interpreter.md) chapters explore two common parts of this process.

## Curiosity Questions

10. What actually happens when you run a program?

   A launcher or operating system starts the program's runtime or executable.
   Language tools may compile source code or prepare bytecode; then the
   runtime or processor executes instructions, requests resources from the
   operating system, and produces output. The exact steps depend on the
   language and platform.

### Rabbit Hole

2. When I type `python app.py`, what happens between pressing Enter and seeing the output?

   The terminal finds and starts the Python executable, passing `app.py` as an
   argument. The operating system creates a process; Python reads the file,
   parses it, and executes its code using its runtime. Calls to print or other
   output functions send data to the terminal, which displays it. Errors can
   stop execution and produce a traceback; the details vary by operating
   system and Python version.
