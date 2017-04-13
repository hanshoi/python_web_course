## Functions ##

Do not repeat yourself, use functions!

* Functions allow you to run same piece of code several times with different arguments.
* Functions will run when they are called, not before.


```python
def print_name(myname):
    print myname

print_name("James Bond")  # this prints now "James Bond" to console
```

A function is always defined with keyword ```def```, followed by function name (used when function is called) and then parentheses ending with :

#### ```def```
```def``` is a keyword argument in python, just like `if`, `with` `and` `for` are as well. Its meaning is to indicate for the computer that following
line is meant to be a function definition.

#### Function Name
Function name is a freeform text that should describe functions usage as well as it can. However python does not limit function names in any way, it is
just a common practice to use proper naming.

```python
# good naming
def say_hello():
    print "hello"

# bad naming
def trololololo():
    print "Be or not to be!"
```

In python function names we use all lower case letters serparated by underscore. This is a system to separate them visually from classes (which are Captitalized for every word, also known as
camel case).

It is generally used that function names should be verbs, as they usually are doing something, ie. get_superhero_logo(), print_hello(), calculate_vector().

#### Blocks
All programming languages separate code in executable blocks. Python uses indent to separate different code blocks from each other, this is either one TAB or 4 spaces, both are equally valid.
A block always starts with a double dot *:* so when you see that sign you know next lines will be indented and will continue to be of one block until some line will be of different indent.

```python
# 1st block
print "hi this is first block"
x = 1

if x == 1:
    # 2nd block
    print "hi this is second block"
    x += 1

    for num in range(x):
        print "this is my 3rd block"

    print "back to 2nd block"

print "back to first block. Man that was lot of Blocks!"
```

#### Function Arguments
Function takes arguments in within it's parentheses, like this:

```python
def calculate_point(x, y):
    print x+y

calculate_point(13, 20)
```

In python you just give the name for you arguments but no types are needed or even possible to give.
You can indicate type with naming though, like _sum_of_vowels_ propably is an integer. So like in everywhere
in Python developers work on trust principle and believe to get right types of arguments.

##### default values
Function arguments can be given default values.

```python
def say_hello(name, times=1):
    for i in range(times):
        print name

say_hello("Jim")
say_hello("Jim", 5)
```

This will by default print word "Jim" on time, but can be changed by giving some value for _times_ argument.

> Arguments with defaults have always to be after, arguments without defaults!

##### *args
There is couple wildcard arguments that can be assigned in function definitions. These are used when you are unsure how many arguments
you will get to your functions. Generally wildcards should be avoided if not necessary but they are a good tool to master.

One _star_ * indicates that following argument is a tuple of all remaining arguments that weren't specifically named.

```python
def myfunction(*args):
    print args

myfunction(1, 2, True, "asdsad")
# this will print >> (1, 2, True, "asdsad")

def second_function(named_argument, *rest):
    print named_argument
    print " ".join(rest)

second_function("Birdie", "Jim", "likes", "apples")
# prints >>
# Birdie
# Jim likes apples
```

> Wildcards come always after named arguments

> Note: *args is common name for unnamed argument tuple

##### **kwargs
** is keyword arguments which are given in a dict. If argument that isn't named is given to function with a keyword it is
not placed into *args but rather into **kwargs and a dict, which may be simpler to handle.

```python
def print_x_y(**kwargs):
    print kwargs
    print kwargs['x']
    print kwargs['y']

print_x_y(x=1, y=2, z=3)
# prints >>
# {'x':1, 'y':2, 'z':3}
# 1
# 2
```

#### Calling Functions
Function is only executed when called.

```python
def myfunc(firstname, lastname):
    print firstname, lastname

myfunc("James", "Bond")  # normal call
myfunc(lastname="Bond", firstname="James")  # call using keywords
```

You can call with either positional arguments. This is when you use argument position to indicate which named argument it is. Other way is to use
keyword arguments where you add argument with it's corresponding keyword to indicate to which named argument it is.

> Keyword arguments have always to come after positional arguments when a combination is given.

#### Return
Return values from functions with ```return``` keyword.

```python
def get_name():
    return "Jim Toddler"

name = get_name()
```


### Excercises ###
Use functions and the main if in next execises. Like this:

```python
def my_function():
    return "variable"

if __name__ == "__main__":
    # do program execution here
    print my_function()
```

#### Sum of Vowels
Enter a string and the program counts the number of vowels in the text.

#### Ascii Sum of Vowels
Enchance previous exercise and calculate sum of all ASCII values of vowels in text.

Example:
Sum on "one" is 212, because ASCII value of "o" is 111 and "e" is 101, hence 111+101=212

> ```ord("o")``` is your friend here (tells ASCII value of a letter).

#### Coin Flip Simulator
Write some code that simulates flipping a single coin however many times the user decides.
The code should record the outcomes and count the number of tails and heads.

##### Cheat of the day
Use module random and from it either function choice() or randint().

```python
import random
random.choice([True, False])
random.randint(0, 1)
```

#### Tick-Tack-Toe ####

Our first game! Let's make our first game with creating a tick-tack-toe game.

* 3x3 map will be used
* Two player hotseat game (players input after each other)
* User may select where they will put their mark
* After each input program will print out the current situation
* After each input program will make winner evaluation and declare winner and exit program if a winner is found.

##### Cheat of the day #####

*raw_input()* and *input()* functions are your friends here. With those you can capture
input from user while program is running.

```python
command = raw_input("Where do you want to tack?:")
```


