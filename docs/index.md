This tutorial is intended for developers who have had experience coding in other languages. At a later point, I will revise this to be readable for beginners. 

I will be using Python 3 and cover introductory to intermediate Python concepts, from basic syntax to object-oriented programming. This will also go over Python features that could prove useful to developers. This will neither go over popular Python modules like numpy, scipy, requests, etc, nor teach data structures and algorithms fundamentals.

## What is Python?

Python is a dynamically-typed, garbage-collected, strongly-typed, interpreted language.

- Dynamically-typed -> variable types is checked at runtime; not known at compile time (duck-typing)
- Garbage collected -> automatic memory management
- Strongly-typed -> forbids operations between distinct types (eg cannot add strings and ints together)
- Interpreted -> Python source code is compiled to byte code, which is run by an interpreter (can be thought of as Python's virtual machine)
## Why use Python?
- Very easy to learn -> easy to read and write programs
- Supports multiple programming paradigms: concurrency, functional, generic, OOP, structural, etc.
- Can be used as a scripting language
- Lots of libraries (especially in scientific computing) and community support
### Why should I not use Python?
- Python is slower compared to other lower-level languages like C, C++, Java
    - Especially important for high-scale, traffic-heavy applications
    - Demonstrated in that serious competitive coders never use Python, but instead use C, C++, Java
- Higher likelihood of runtime errors due to weaker typing compared to strictly typed languages
- High memory and power consumption - especially for computation-intensive programs like those of machine learning
- Lack of UI/visual components -> it is barely used for mobile computing

## Who or what uses Python?
- One of the most popular programming languages of 2020
- Companies
    - NASA
    - Facebook
    - Google
    - Amazon
    - Spotify
- Applications:
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
