# #ALX_BE

## Foundamentals
A lot of concepts are being introduced out here

### Resources
This is a list of resources that privide information

#### Videos
 - [Python Simplified](https://www.youtube.com/@PythonSimplified)

### Git and GitHub

### Advanced Git Commands
- .gitignore files
More information about the .gitignore templates for different programming
languages at the [.gitignore repo](https://github.com/github/gitignore)

### Shell
These are some resources that help to ubderstand the shell very well

- [The Shell](http://linuxcommand.org/lc3_lts0010.php)

- [Navigation](http://linuxcommand.org/lc3_lts0020.php)

- [Working with commands](http://linuxcommand.org/lc3_lts0060.php)

- [Looking Around](http://linuxcommand.org/lc3_lts0030.php)

- [Manipulating Files](http://linuxcommand.org/lc3_lts0050.php)

- [File permissions](https://linuxize.com/post/understanding-linux-file-permissions/)

- [File Permissions in 5](https://www.youtube.com/watch?v=LnKoncbQBsM)

- [Permissions](http://linuxcommand.org/lc3_lts0090.php)

#### Advanced Commands
- [Grep](https://www.gnu.org/software/grep/manual/grep.html)

### Problem Solving
- [14 problem solving strategies](https://www.indeed.com/career-advice/career-development/problem-solving-strategies)

## Paradigms and Algorithms

### Paradigms
OOP in computer programming focuses on how to break up the requirements into simple, reusable classes that can be used to blueprint instances of objects. Overall, implementing OOP allows for better data structures and reusability, saving time in the long run.

- [educative: Object Oriented Programming](https://www.educative.io/blog/object-oriented-programming)

## Python

- [Geek for geeks](https://www.geeksforgeeks.org/introduction-to-python/)

### Match case (Conditional Statements)

The __match__ statement is used to compare a **variable** against a different condition.
The __case__ statement specify the conditions and corresponding message is printed if the condition is met.
The base _wildcard is used to catch any invalid inputs.

#### Basic

```py
day = input("Enter day of the week: ").lower()

match day:
    case 'monday':
        print("ugh, just another first day")
    case 'tuesday':
        print("Second day init")
    case 'wednesday':
        print('midweek is here for you')
    case 'thursday':
        print("Almost there. hold on tight")
    case 'friday':
        print('we say TGIF  yaaaaay')
    case 'saturday' | 'sunday' :
        print("Weekend vibes")
    case _:
        print('invalid day entered')
```
Towards the end of the code block, the pipe `\` is used to include two responses like using `or`.

#### Advanced
In the example of the `number guessing game` the case section had an if statement like so:

```py
# This shows the challenge for match case

import random

guess = int(input("Guess a number: "))

secret_number = random.randint(1,20)

match guess:
    case guess if guess > secret_number:
        print("Your guess is too high")
    case guess if guess < secret_number:
        print("your guess is kind of low")
    case guess if guess == secret_number:
        print("Congratulations, You guessed it")
```
In the `case` section, the `if` keyword is used to add an exra condition to check, besides the value itself.

Think of it like a double-check:
 - "Is it a toy car?" (case 1)
    - "and is it red?" (if)
 - "Is it a doll?" (case 2)
    - "and is it wearing a hat?" (if)

The `if` clause in the `case` statement is like an additional filter, to further refine the match. It is like saying "Not only does it have to be a toy car, but it has to be red".

**Making it fewer**
```py
match guess as x:
    case x if x > secret_number:
        print("Your guess is too high")
    case x if x < secret_number:
        print("your guess is kind of low")
    case x if x == secret_number:
        print("Congratulations, You guessed it")
```

The code is written as 
`case x if x < secret_number` means 
is the value `x` less than the `secret_number`?

### Namespaces
A **namespace** is a list of methods, functions and classes that are available to a calling program.
Information on namespaces is found in the [Namespaces Documentation](https://docs.python.org/3/faq/programming.html).

Just `ctrl + F` and search `namespace` to display the outputs.



