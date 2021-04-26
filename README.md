# graph-theory-project

## Introduction

Our third year project for Graph Theory consisted of writing a program that searches a text file using a regular expression.
The program must take a regular expression and the name or path of the file as command line arguments and output the lines of the file matching the regular expression.

## What is a regular expression?

A **regular expression** is a special sequence of characters that defines a pattern for complex string-matching functionality. 
Regular expressions can also be used from the command line and in text editors to find text within a file.
They are useful for validating input and are constructed using simple concepts such as conditionals and loops.

#### Special characters

- **.** means concatenate. So, a.b means an a followed by a b.
- **|** means or. So, a|b means an a or a b.
- **∗** means zero or more times. So, a∗ means zero or more a’s.

#### Precedence 

1. Always apply **∗** first.
2. Apply **.** after **∗** but before **|**.
3. Apply **|** last.
4. Treat bracketed groups as individual characters.









