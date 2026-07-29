
Given your available time:

- Weekdays: ~5 hours/week
- Weekends: ~6–8 hours/week
- Total: ~11–13 hours/week
- Over 10–12 weeks: ~120–150 focused hours

That is enough time to:

- build strong systems fundamentals
- become productive in C
- understand Linux internals at a practical level
- complete **1 substantial project + 1 smaller supporting project**

It is _not_ enough time to deeply master:

- compilers
- kernels
- advanced networking
- distributed systems

So the roadmap should optimize for:

1. maximum conceptual leverage
2. transferable systems understanding
3. production engineering habits
4. realistic scope

The biggest mistake would be trying to “learn all of C.”  
You actually want:

- systems thinking
- memory awareness
- OS understanding
- debugging discipline

C is just the vehicle.

---

# Recommended Outcome After 3 Months

By the end, you should be able to:

- comfortably read low-level codebases
- understand memory ownership clearly
- debug crashes with `gdb`
- reason about stack/heap/layout
- understand Linux process/file/socket abstractions
- build and debug native binaries
- understand performance basics
- write non-trivial C programs confidently

And ideally complete:

### Main Project

A production-style HTTP server OR mini shell

### Secondary Project

A custom allocator OR thread pool OR Redis-like in-memory store

That combination gives enormous leverage.

---

# What NOT To Spend Time On

Avoid:

- obscure C syntax trivia
- competitive programming
- advanced algorithms
- GUI programming
- embedded hardware
- writing a kernel
- deep compiler theory

Those are lower ROI for your current goal.

---

# High-Level Roadmap

|Phase|Duration|Goal|
|---|---|---|
|Foundations|Week 1–2|C + memory model|
|Systems Core|Week 3–4|Linux/processes/files|
|Networking + Concurrency|Week 5–6|sockets + event loops|
|Main Project|Week 7–9|HTTP server or shell|
|Advanced Memory + Debugging|Week 10|allocator + tooling|
|Polish + Production Workflow|Week 11–12|profiling/testing/build systems|

---

# Phase 1 — C + Computer Memory Fundamentals (Weeks 1–2)

Goal:  
Understand what memory actually is.

## Concepts

### C Core

- [x] pointers
- [x] arrays vs pointers
- [x] structs
- [x] stack vs heap
- [ ] manual memory management
	- [x] Dynamic array
	- [ ] Single linked list
	- [ ] Double linked list
	- [ ] StringBuilder/String Library
- [ ] function pointers
- [ ] const correctness

### Memory Concepts

- [ ] virtual memory
- [ ] memory layout of a process
- [ ] alignment
- [ ] padding
- [ ] endianness
- [ ] binary representation

### Compilation Pipeline

- preprocessing
- compilation
- linking
- ELF binaries
- static vs dynamic linking

### Essential Linux APIs

- `malloc/free`
- `memcpy`
- `open/read/write/close`
- `mmap`

---

## Exercises

### Tiny Programs

Write:

- dynamic array
- string library
- hash map
- arena allocator

Avoid tutorial-copying.

---

## Tooling (VERY IMPORTANT)

Learn immediately:

- `gcc`
- `make`
- `gdb`
- `valgrind`

You should use:

```bash
-Wall -Wextra -Werror
```

from day one.

---

# Phase 2 — Linux Systems Fundamentals (Weeks 3–4)

Goal:  
Understand the OS abstractions developers usually ignore.

---

## Concepts

### Processes

- `fork`
- `exec`
- `waitpid`
- process lifecycle

### File Descriptors

- stdin/stdout/stderr
- pipes
- redirection

### Signals

- interrupts
- signal handlers
- SIGINT/SIGTERM

### Syscalls

- user space vs kernel space
- syscall overhead

### Filesystem Basics

- inodes
- buffering
- page cache

---

## Project #1 (Smaller)

Build a mini Unix shell.

Features:

- command execution
- piping
- redirection
- background jobs

This project teaches:

- processes
- file descriptors
- pipes
- signals

This is arguably the best beginner systems project.

---

# Phase 3 — Networking + Concurrency (Weeks 5–6)

Goal:  
Understand how backend systems actually communicate.

---

## Concepts

### Networking

- sockets
- TCP lifecycle
- blocking vs non-blocking I/O
- epoll/select/poll

### HTTP Basics

- request parsing
- headers
- persistent connections

### Concurrency

- threads
- mutexes
- race conditions
- deadlocks
- thread pools

### Performance Basics

- cache locality
- syscalls cost
- memory allocation overhead

---

## Mini Exercises

Build:

- TCP echo server
- thread pool
- simple HTTP parser

---

# Phase 4 — Main Project (Weeks 7–9)

Choose ONE.

---

# Option A (Recommended): HTTP Server

This has the highest modern backend relevance.

## Features

### Core

- sockets
- HTTP parsing
- static file serving

### Intermediate

- keep-alive
- routing
- logging
- thread pool

### Advanced (Optional)

- epoll
- zero-copy sendfile
- request queue

---

## What You Learn

- kernel/network interaction
- concurrency
- memory ownership
- resource cleanup
- production debugging

This is extremely high ROI.

---

# Option B: Redis-like In-Memory Store

Features:

- TCP protocol
- hash table
- expirations
- persistence

This teaches:

- data layout
- memory efficiency
- protocol design

Excellent project too.

---

# Phase 5 — Debugging + Memory Deep Dive (Week 10)

Goal:  
Become dangerous with debugging.

---

## Learn Properly

### gdb

- stack traces
- breakpoints
- memory inspection
- register inspection

### valgrind

- leaks
- invalid access
- use-after-free

### Sanitizers

- ASAN
- UBSAN

### Linux Tools

- `strace`
- `ltrace`
- `perf`

---

## Secondary Project

Choose one:

### Option 1

Custom allocator (`malloc` clone)

### Option 2

Arena allocator library

### Option 3

Lock-free queue (harder)

Allocator projects massively improve memory understanding.

---

# Phase 6 — Production Workflow + Polish (Weeks 11–12)

This is where the learning solidifies.

---

## Learn

### Build Systems

- Makefiles
- basic CMake

### Testing

- unit testing
- stress testing
- fuzzing basics

### Profiling

- flamegraphs
- `perf`
- timing bottlenecks

### Linux Knowledge

- `/proc`
- memory maps
- process stats

---

# Recommended Weekly Structure

## Weekdays (1 hour)

### Best Use

- 30 min learning
- 30 min implementation

Consistency matters more than marathon sessions.

---

## Weekends (3–4 hours/day)

Use for:

- larger implementation work
- debugging
- refactoring
- reading systems docs

This is where projects move forward.

---

# Recommended Resources

## Best Overall Systems Book

Computer Systems: A Programmer's Perspective

---

## Best Practical Linux Book

The Linux Programming Interface

---

## Best C Reference

Modern C

---

## Best Runtime/VM Book

Crafting Interpreters

(Optional for now.)

---

# Technologies You Should Actually Use

## Editor

- Neovim OR VSCode
    

## Compiler

- GCC
    
- Clang
    

## Platform

- Linux preferred
    
- WSL acceptable
    

---

# What Success Looks Like

After this roadmap, you should feel comfortable:

- reading C codebases
    
- understanding memory ownership
    
- debugging segfaults
    
- reading assembly occasionally
    
- understanding sockets/processes/files
    
- reasoning about performance
    
- understanding what high-level runtimes abstract away
    

That foundation transfers directly into:

- Go
    
- Rust
    
- JVM internals
    
- databases
    
- distributed systems
    
- backend engineering
    
- performance optimization
    

And importantly:  
you’ll think differently about software afterward.