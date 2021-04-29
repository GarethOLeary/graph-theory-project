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

#### Examples 
1. Check that an email address is valid.
2. Find phone numbers in a text file.

## How do regular expressions differ across implementations?

Regex definition described at 'https://www3.ntu.edu.sg/home/ehchua/programming/howto/Regexe.html'
> Regex is supported in all the scripting languages (such as Perl, Python, PHP, and JavaScript), as well as general purpose programming languages such as Java and even word processors such as Word for searching texts. 

Regular expressions are an important component of programming languages but they do differ across implementations.
Programming languages have similar regular expression syntaxes, so there is a chance of them compiling after modification when re-used. 
Developers should be careful when it comes to copying and pasting regular expressions, especially when the langauge origin is unknown as that could lead to program misbehaviour or portability problems.

#### Semantic portability problems
These problems can occur when two programming languages compile but have different match behaviour. If the regex is long, it could be hard to figure out the problem.

#### Performance portability problems
Most programming languages implement their own regex engine which they differ in the syntax and semantics they support, but they also differ in their performance, the time and/or space cost to perform a match. Performance portability problems include slow software which is frustrating for any developer.

#### Syntactic portability problems
Runtime exceptions and program crashes can be caused by regexes compiling in some languages and not others. 

Information retrieved from 'https://davisjam.medium.com/why-arent-regexes-a-lingua-franca-esecfse19-a36348df3a2'

## Can all formal languages be encoded as regular expressions?

#### What is a formal language?

As described by Wiki 'https://en.wikipedia.org/wiki/Formal_language'
> In logic, mathematics, computer science, and linguistics, a formal language consists of words whose letters are taken from an alphabet and are well-formed according to a specific set of rules.

The alphabet of a formal language is made up of a  set of symbols and letters from which the strings of the language may be formed, these strings are known as words. 

Programming languages are an example of a formal language, which is defined by two sets of rules:

**Syntax:** precise rules that tell you the symbols you are allowed to use.

**Semantics:** precise rules that tell you the meanings of the symbols and legal expressions.

## Shunting Yard Algorithm

The shunting yard algorithm was invented by **Edsger Dijkstra** who was a famous Dutch computer scientist, with the purpose of converting an infix expression to postfix.
The input of this algorithm consists of two parts, the output queue and the operator stack. 
Each operator gets assigned its correct operator and takes into account the order of precedence.

#### Pseudocode of the algorithm

<img width="540" alt="shunt" src="https://user-images.githubusercontent.com/48318455/116535641-e2203d80-a8db-11eb-8c17-fa88f173018e.PNG">

#### Precedence Table 

| Order | Order Of Precedence | 
|---|---|
| ^ | 3 |
| / | 2 |
| * | 2 |
| + | 1 |
| - | 1 |

## Thompson's Construction

Thompson's construction is an algorithm to construct a Non-determistic Finite Automation(NFA) from a regular expression. 

#### Rules:

1. The NFA representing the empty string.

![image](https://user-images.githubusercontent.com/48318455/116588065-00556000-a913-11eb-81c7-f16efb053bbd.png)

2. If the regular expression is just a character.

![image](https://user-images.githubusercontent.com/48318455/116588409-7063e600-a913-11eb-9575-8f53aef9a741.png)

3. The union operator is represented by a choice of transitions from a node.

![image](https://user-images.githubusercontent.com/48318455/116588604-a7d29280-a913-11eb-8a5c-d4cf84452015.png)

4. Concatenation simply involves connecting one NFA to the other.

![image](https://user-images.githubusercontent.com/48318455/116588711-c9cc1500-a913-11eb-9c21-04f08ec10c6b.png)

5. The Kleene closure must allow for taking zero or more instances of the letter from the input.

![image](https://user-images.githubusercontent.com/48318455/116588226-2ed33b00-a913-11eb-9c89-ab6bda3ea8af.png)

Images sourced from 'https://en.wikipedia.org/wiki/Thompson%27s_construction#Rules'


## Lab Work 

'https://github.com/GarethOLeary/GraphTheory_WeeklyExercises'

## Resources 

'https://brilliant.org/wiki/shunting-yard-algorithm/'

'https://en.wikipedia.org/wiki/Formal_language'














