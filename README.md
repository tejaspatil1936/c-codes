# c-codes

A collection of standalone C programs covering core language fundamentals, written and compiled while learning C.

## Overview

This repository holds 69 individual C source files (plus one C++ file) written as independent, self-contained programs. Each file has its own `main()` function and solves one small problem — there is no shared library code or single entry point tying them together. The exercises range from a first `printf("Hello World")` up through arrays, functions, recursion, and short algorithmic problems.

## Features

The programs cover the following topics:

| Topic | Example files |
|---|---|
| Basic I/O (`printf`/`scanf`) | `hello.c`, `hi.c`, `input.c`, `code.c` |
| Conditionals (`if`/`else`) | `ifelse.c`, `exp4.c`, `p5.c`, `abc.c` |
| `switch` statements | `switchcase.c`, `aq8.c`, `exp5.c`, `ps 9.c` |
| Loops (`for`, `while`, `do-while`) | `loops.c`, `while.c`, `aq1.c`, `exp6.c`, `asdfghjkl.c` |
| Pattern printing with nested loops | `pattern1.c`, `pattern2.c`, `aq6.c`, `aq7.c`, `cc2.c`, `p2.c` |
| Arrays and matrices | `array.c`, `arrays.c`, `countevenodd.c`, `p7.c`, `p8.c` |
| Functions (with/without arguments and return values) | `functions0.c`, `functions1.c`, `functions2.c`, `exp8.c` |
| Recursion | `recursivefunction.c` (recursive factorial) |
| `goto` statement | `goto.c` |
| Type casting | `typecasting.c` |
| Numeric/math problems (primes, factorials, quadratic roots, series sums, geometry) | `prime.c`, `factorial.c`, `random.c`, `p6.c`, `p1.c`, `p3.c`, `p10.c`, `ps 1.c` |
| Strings and character arrays | `p9.c`, `practice.c` |
| Short judge-style problems (sums, divisibility checks, conditionals framed as word problems) | `cc1.c`, `cc3.c`, `cc4.c` |

## Tech Stack

- **Language:** C (99/89-style single-file programs using the standard library — `stdio.h`, `math.h`)
- **Secondary language:** C++ (`a.cpp`, a single "Hello World" example using `iostream`)
- **Compiler:** GCC — the committed binaries `a.out` and `p4` are ELF 64-bit executables built with GCC 11 on Ubuntu 22.04

## Project Structure

All files sit at the repository root; there are no subdirectories. Filenames follow a few naming patterns from different practice sessions:

```
c-codes/
├── hello.c, hi.c, hii.c, code.c ...   # early I/O exercises
├── aq1.c, aq6.c ... aq8.c             # "assignment question" style exercises
├── ps 1.c ... ps 10.c                 # numbered problem-set exercises (note: filenames contain a space)
├── exp.c, exp4.c ... exp10.c          # numbered "experiment" exercises
├── p1.c ... p10.c                     # numbered practice programs
├── cc1.c ... cc7.c                    # short algorithmic/judge-style problems
├── a.cpp                              # single C++ example
├── a.out, p4                          # compiled binaries checked into the repo
└── README.md
```

A few files are placeholders with no content (`main.c`, `dcg.c`, `cc7.c` are empty), and `hello copy.c` duplicates `hello.c`.

## Getting Started

### Prerequisites

- A C compiler such as GCC or Clang
- (Optional, for `random.c` and `p6.c`) a linker flag for the math library, since both use `sqrt()` from `math.h`

### Run locally

Each file is independent and can be compiled and run on its own. For example:

```bash
gcc hello.c -o hello
./hello
```

For a file that uses `math.h`:

```bash
gcc random.c -o random -lm
./random
```

Filenames containing spaces (the `ps *.c` files) need to be quoted:

```bash
gcc "ps 1.c" -o ps1
./ps1
```

### Build

There is no build script or Makefile — each program is compiled individually with `gcc <file>.c -o <output>` as shown above.

## Usage

Most programs prompt for input via `scanf` and print a result via `printf`. For example, `factorial.c` asks for an integer and prints its factorial; `prime.c` asks for a number and reports whether it is prime; `pattern1.c` asks for a size `n` and prints a triangle of asterisks.

## Future Improvements

- Add a `.gitignore` for compiled output — `a.out` (built from `prime.c`) and `p4` (built from `p4.c`) are currently tracked binaries and don't need to be in version control.
- Remove the empty placeholder files (`main.c`, `dcg.c`, `cc7.c`) and the duplicate `hello copy.c`.
- Rename the `ps *.c` files to remove the space (e.g. `ps1.c`) to avoid needing to quote them when compiling.
