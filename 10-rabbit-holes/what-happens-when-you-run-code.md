# What Happens When You Run Code?

Running code involves a chain of steps from editing source text to observing a program's behavior.

## Follow the trail

1. **Command:** When you enter `python app.py`, the shell resolves `python`
   using its command lookup rules (often the `PATH`) and starts the interpreter
   with `app.py` as an argument.
2. **Process:** The operating system creates a process, gives it a virtual
   address space and resources, and schedules its thread to run on a processor.
3. **Parsing and preparation:** Python reads and parses the source. CPython
   normally compiles it to bytecode; other Python implementations can differ.
4. **Execution:** The Python runtime evaluates the bytecode, performs
   calculations, and calls operating-system services through runtime
   interfaces when needed.
5. **Output:** A call such as `print()` writes text to standard output. The
   terminal displays it; errors may instead produce a traceback on standard
   error.
6. **Exit:** When the script finishes or fails, the process exits with a
   status. The operating system releases its process resources; data must
   have been saved to persistent storage if it needs to survive.

## Explore further

Connect the ideas in [how code runs](../01-programming-basics/how-code-runs.md), [compilers](../03-how-programs-run/compiler.md), and [processes](../03-how-programs-run/process.md).
