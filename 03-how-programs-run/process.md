# Process

A process is a running instance of a program with its own execution state and resources.

## What you'll learn

- How a program becomes a process
- What memory and resources an operating system manages for it
- How processes are isolated from one another

## Explore further

See [threads](threads.md) to learn how a process can have multiple paths of execution.

## Curiosity Questions

31. Who receives the `python app.py` command?

   The command is first handled by the command-line shell or terminal
   environment. The shell finds the `python` executable using its command
   lookup rules, launches it, and passes `app.py` as an argument.

32. How does the operating system know where Python is?

   Usually the shell searches directories listed in the `PATH` environment
   variable for an executable named `python` (or a platform-specific
   equivalent). If the command is given with a full path or through a
   launcher, that mechanism can locate it differently.

33. What is a process?

   A process is a running program instance managed by the operating system.
   It has its own virtual address space and resources, such as open files,
   and contains one or more threads. The OS schedules its threads to use
   processor time.

35. Where does the Python interpreter run?

   The interpreter is itself a program running as a process on the operating
   system. The processor executes its machine instructions; the interpreter
   then reads and runs the Python program within that process.

40. What happens when the program crashes?

   An unhandled error may stop the program and produce an error message or
   traceback. A severe fault can cause the operating system to terminate the
   process; the OS releases its process resources, while data not saved to
   persistent storage may be lost.

### Rabbit Hole

8. How does a program know that another program has crashed?

   A program usually learns through an operating-system or runtime signal:
   for example, a parent process can observe a child process's exit status.
   Separate services commonly use timeouts, health checks, or missed
   heartbeats to detect failure. A network timeout alone cannot prove whether a
   remote service crashed or is merely delayed or unreachable.
