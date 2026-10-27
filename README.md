# Python

Course notebooks for **Python**, a multi-level course that takes you from first principles to professional proficiency. Work through the levels as you need them: stop after any level, skip the ones you already know, or come back later. Each level assumes the ones before it, and Level 1 assumes no programming experience at all.

You work in [Jupyter](https://jupyter.org/) notebooks: each one teaches one idea with small runnable examples, then gives you exercises that check your answers as you go.

## Getting started

You need [uv](https://docs.astral.sh/uv/), a fast Python tool that also installs the right version of Python (3.12) for you. Install it from the terminal:

```bash
# macOS or Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Clone the repository and start Jupyter:
 
```bash
git clone https://github.com/ankurdivekar/python-course.git
cd python-course
uv sync
uv run jupyter lab
```

Then open the `notebooks` folder and start with `00_Welcome_and_Setup.ipynb`. It covers how notebooks work and has a troubleshooting checklist.

For Levels 1 and 2 that is all you need. From Level 3 on, notebooks need extra packages, and each of those notebooks tells you the exact command. In general, to work at **Level N** (which includes everything from the levels before it):

```bash
uv sync --group levelN
uv run --group levelN jupyter lab
```

## How the course is organised

| Level | Theme | After finishing you can... |
|---|---|---|
| 1. Foundations | Setup, data types, input, decisions, loops | write interactive programs with variables, text, numbers, decisions and loops |
| 2. Data Structures and Functions | Lists, tuples, dicts, sets, functions | organise data and structure code into reusable functions |
| 3. Practical Python | Debugging, exceptions, testing, files, modules, data formats, scripts | write programs that handle errors, read and write files, and run as scripts |
| 4. Idiomatic Python and OOP | Comprehensions, functional tools, classes | write idiomatic Python and model problems with classes |
| 5. Python for Data | NumPy, Matplotlib, pandas | load, clean, analyse and visualise real datasets |
| 6. Advanced Language Features | Closures, decorators, iterators, context managers, typing | use Python's deeper features with confidence |
| 7. Software Design | Refactoring, SOLID, design patterns | design maintainable, extensible code |
| 8. Software Engineering Practice | Packaging, logging, CLIs, git, tooling, CI, docs | build, test and ship a professional-quality library |
| 9. Performance and Concurrency | Memory model, profiling, threads, processes, asyncio | find bottlenecks and choose the right concurrency model |
| 10. Python in the Real World | HTTP, databases, web APIs, automation | build and deploy real applications |

Notebook file names are numbered in the order you should work through them, continuing across levels. New material is added level by level.

## Notebook index

### Level 1 · Foundations

| # | Notebook | What you learn |
|---|---|---|
| 00 | [Welcome and Setup](notebooks/00_Welcome_and_Setup.ipynb) | What programming is, how notebooks work, setup and troubleshooting |
| 01 | [Your First Programs](notebooks/01_Your_First_Programs.ipynb) | `print()`, comments, reading error messages |
| 02 | [Variables and Assignment](notebooks/02_Variables_and_Assignment.ipynb) | Naming values, types, swapping |
| 03 | [Numbers and Math](notebooks/03_Numbers_and_Math.ipynb) | Integers, floats, operators, the `math` module |
| 04 | [Strings](notebooks/04_Strings.ipynb) | Creating, indexing and slicing text |
| 05 | [String Methods and Formatting](notebooks/05_String_Methods_and_Formatting.ipynb) | Cleaning text, f-strings, Unicode |
| 06 | [User Input and Type Conversion](notebooks/06_User_Input_and_Type_Conversion.ipynb) | `input()`, `int()`, `float()`, `bool()` |
| 07 | [Booleans and Comparisons](notebooks/07_Booleans_and_Comparisons.ipynb) | `True`/`False`, `and`/`or`/`not`, truthiness |
| 08 | [Conditionals](notebooks/08_Conditionals.ipynb) | `if`, `elif`, `else`, `match` |
| 09 | [While Loops](notebooks/09_While_Loops.ipynb) | Repeating until something changes |
| 10 | [For Loops and Range](notebooks/10_For_Loops_and_Range.ipynb) | `for`, `range()`, `enumerate()`, `zip()` |
| 11 | [Nested Loops and Loop Patterns](notebooks/11_Nested_Loops_and_Loop_Patterns.ipynb) | Grids, common patterns, and the **Level 1 project**: a number-guessing game |

### Level 2 · Data Structures and Functions

| # | Notebook | What you learn |
|---|---|---|
| 12 | [Lists](notebooks/12_Lists.ipynb) | Ordered, changeable sequences; aliasing vs. copying; nested lists |
| 13 | [Tuples and Unpacking](notebooks/13_Tuples_and_Unpacking.ipynb) | Fixed-size groupings, packing and unpacking, `*` unpacking |
| 14 | [Dictionaries](notebooks/14_Dictionaries.ipynb) | Key-value lookup, counters, nested dicts |
| 15 | [Sets](notebooks/15_Sets.ipynb) | Unique collections and set operations |
| 16 | [Choosing the Right Collection](notebooks/16_Choosing_the_Right_Collection.ipynb) | Comparing list, tuple, dict, set and string; mixed structures |
| 17 | [Functions](notebooks/17_Functions.ipynb) | `def`, `return`, docstrings, reuse |
| 18 | [Function Arguments and Scope](notebooks/18_Function_Arguments_and_Scope.ipynb) | Keyword and default arguments, `*args`/`**kwargs`, scope, mutable defaults |
| 19 | [Recursion and Function Design](notebooks/19_Recursion_and_Function_Design.ipynb) | Recursion (optional), small single-purpose functions, decomposing programs |

Levels 3 to 10 are coming.

## How the notebooks work

Every notebook has the same shape: learning goals, why the idea matters, short explanations with runnable examples, a section on common mistakes, graded exercises (warm-up, practice, stretch) and a recap.

- **Run cells one at a time** with `Shift + Enter`. Some cells are marked *"⚠️ Expected to fail"*: they show an error on purpose so you learn to read it, and *Run All* will stop there.
- **Exercises check themselves.** Write your answer in the starter cell and run it, then run the check cell below it. `check(answer, expected)` compares a value; `check_output(expected_text)` re-runs your most recent code cell and compares what it prints (supplying `input()` answers for you where needed). Both live in [`src/course_tools.py`](src/course_tools.py).
- **Try before you peek.** If a hint is offered, open it only after you've tried.

## License

Code is MIT-licensed and course text is CC BY-SA 4.0. See [LICENSE.md](LICENSE.md).

## Updates

This repository is updated automatically as new material is released. Run `git pull` regularly to get the latest notebooks.
