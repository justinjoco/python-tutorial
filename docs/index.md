This tutorial is intended for those who have had at least some experience coding in other languages. The goal is for readers to understand how to read and write basic to non-trival programs in Python.

 I've separated this tutorial into two parts: `Need to Know` consists of concepts that those who learn Python should know. `Good to Know` consists of supplemental features that can enhance how you use Python, but are not necessary to make non-trival programs and applications. 

I will be using Python3.6 (since this version includes "type-hinting") and cover introductory to intermediate Python concepts, from basic syntax to object-oriented programming. This will neither go over popular Python modules like numpy, scipy, requests, etc, nor teach data structures and algorithms fundamentals.

## What is Python?

Python is a dynamically-typed, garbage-collected, strongly-typed, interpreted language.

- Dynamically-typed -> variable types is checked at runtime, not at compile time (duck-typing)
- Garbage collected -> automatic memory management
- Strongly-typed -> forbids operations between distinct types (eg cannot add strings and ints together)
- Interpreted -> Python source code is compiled to byte code, which is run by an interpreter (can be thought of as Python's virtual machine).

As an FYI, CPython is Python's most widely used implementation.
## Why use Python?
- It's very easy to learn, to read, and to write programs
- It supports multiple programming paradigms: concurrency, functional, generic, OOP, structural, etc.
- It can be used as a scripting language
- There are many libraries in different fields, including but limited to the following:
    - machine learning and artificial intelligence (ML/AI)
    - web development
    - scientific computing
- There is plenty of community support, in terms of documentation and a plethora of questions asked and answered (StackOverflow is your friend).
### Why should I not use Python?
- Python is slower compared to other lower-level languages like C, C++, Java
    - This is especially important for high-scale, traffic-heavy applications
    - This is further demonstrated in that serious competitive coders almost never use Python, but instead use C, C++, Java
- There is a higher likelihood of runtime errors due to weaker typing compared to stricter typed languages
- Running Python programs can consume lots of power and memory, especially for computation-intensive programs like those of machine learning
- There is a lack of UI/visual components -> it is barely used for mobile computing

## Who or what uses Python?
- Python is one of the most popular programming languages of 2020
- Multiple high-profile companies use it in some of their projects:
    - NASA
    - Facebook
    - Google
    - Amazon
    - Spotify
- Popular applications use it, such as:
    - Dropbox - file hosting service (originally written in Python -> migrated to Go)
    - SciPy - scientific computing library
    - The Sims 4 - life simulation video game
    - Django - MTV web framework
    - Flask - web framework

## Hello World
Unlike lower-level programming languages, there is no requirement to make a `main` function to run a simple program. One can simply write one line of code to make a `Hello World` program, like the following:
``` python
print("Hello World")
```
Fortunately, you can certainly make a `Hello World` program with a `main` function-like structure using the special variable `__name__`:
``` python
def main():
    print("Hello World")

if __name__ == "__main__":
    main()
```
If you run a specific Python file, then that file will be treated as the `main` file, in which the following code block will run:
```python
if __name__ == "__main__":
    main()
```
