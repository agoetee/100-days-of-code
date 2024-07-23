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

*Highlights*
It’s good practice if you import modules in the following order:

 1. standard library modules – e.g. sys, os, argparse, re

 2. third-party library modules (anything installed in Python’s site-packages directory) – e.g. dateutil, requests, PIL.Image

 3. locally developed modules

 ## Exception Handling

 ### Custom Exception
 Custom exceptions are user-defined exception classes that you create to handle specific errors or exceptional situations in your code. By deriving custom exceptions from the base Exception class in Python, you can create more meaningful and specific error messages for your applications.

 ```py
 class OutOfStockError(Exception):
    """Custom exception for handling out-of-stock items."""

    def __init__(self, item_name):
        self.item_name = item_name

    def __str__(self):
        return f"Sorry, the item '{self.item_name}' is out of stock."

# Sample Product Inventory
product_inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 0,  # Out of stock
    "grapes": 3
}
 ```

Then call a function to utilize the class:

```py
def purchase_item(item, quantity):
    try:
        if product_inventory[item] == 0:
            raise OutOfStockError(item)
        else:
            print(f"Purchase successful: {quantity} {item}(s)")
            product_inventory[item] -= quantity
    except KeyError:
        print(f"Sorry, '{item}' is not available in our inventory.")

# Testing the Custom Exception
try:
    purchase_item("apple", 3)  # Purchase successful
    purchase_item("orange", 1)  # Raises OutOfStockError
    purchase_item("watermelon", 1)  # Item not available
except OutOfStockError as e:
    print(e)  # Output:
```

## Databases

### The Relational model

Resources

 - [A good overview of Databases](https://www.techopedia.com/6/28832/enterprise/databases/introduction-to-databases#:~:text=A%20database%2C%20in%20the%20most,store%2C%20manage%20and%20retrieve%20information)

  - [Databases by Digital Ocean](https://www.digitalocean.com/community/conceptual-articles/an-introduction-to-databases)



