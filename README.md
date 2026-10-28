# C Memory Management

This repository records my study of memory management in C. It contains the exercises I solved, organized by topic, along with notes written in my own words about what I learned and which mistakes I made along the way.

I am a Software Engineering student, and the goal is to understand how C handles memory well enough to build my own data structures without relying on abstractions.

## How to compile and run

Every exercise is compiled with warnings enabled, debug symbols, and AddressSanitizer, which catches memory leaks and invalid accesses at runtime:

```bash
gcc -Wall -Wextra -g -fsanitize=address exercise.c -o exercise
./exercise
```

For a second opinion on leaks, I also run the programs under Valgrind:

```bash
valgrind --leak-check=full ./exercise
```

AddressSanitizer and Valgrind should not be combined in the same run, so I compile a separate binary without `-fsanitize=address` when using Valgrind.

## Roadmap

| # | Topic | Contents | Status |
|---|-------|----------|--------|
| 01 | [Basic pointers](01-basic-pointers/) | `&`, `*`, pointer to pointer, passing by reference | In progress |
| 02 | [Pointers and arrays](02-pointers-arrays/) | Pointer arithmetic, arrays as function parameters, `sizeof` pitfalls | Not started |
| 03 | [malloc and free](03-malloc-free/) | Dynamic allocation, `NULL` checks, freeing memory | Not started |
| 04 | [calloc and realloc](04-calloc-realloc/) | Zero-initialized allocation, resizing blocks | Not started |
| 05 | [Dynamic structs](05-dynamic-structs/) | `struct` with heap allocation, nested allocations | Not started |
| 06 | [Data structures](06-data-structures/) | Linked list, stack, queue | Not started |
| 07 | [Final project](07-final-project/) | Dynamic array (vector-like) and/or a simple hash table | Not started |

## Repository structure

```
.
├── README.md
├── .gitignore
├── 01-basic-pointers/
│   ├── ex01_simple_pointer.c
│   ├── ex02_swap.c
│   └── NOTES.md
├── 02-pointers-arrays/
└── ...
```

Each folder has one `.c` file per exercise and a `NOTES.md` with my explanations, the errors I ran into, and how I fixed them.

## Common mistakes

This section grows as I study. Entries so far:

- _Nothing recorded yet._

Examples of what will probably show up here: forgetting to call `free`, using a pointer after freeing it, calling `sizeof` on an array parameter, and not checking whether `malloc` returned `NULL`.

## Tools

- `gcc` for compilation
- AddressSanitizer (`-fsanitize=address`) for runtime memory checks
- Valgrind for leak detection
- Git and GitHub for version control, with one commit per exercise

## About

João Otávio Cardoso Vilela (Jay)

- GitHub: [github.com/JayOta](https://github.com/JayOta)
- Portfolio: [jayota.github.io/Jay_Ota_Portofolio](https://jayota.github.io/Jay_Ota_Portofolio)
- LinkedIn: [linkedin.com/in/jayota](https://linkedin.com/in/jayota)