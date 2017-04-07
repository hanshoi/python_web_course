# Functions #

Do not repeat yourself, use functions!

* Functions allow you to run same piece of code several times with different arguments.
* Functions will run when they are called, not before.

## Excercises

### FizzBuzz
Lets do this classic programming excecise. Print all number from 0 to 100. If number is divisible with 3 then print "Fizz" instead of the number, if the number is divisible with 5 then print "Buzz", if it is divisible with both then print "Fizz Buzz".

### ls
Make your own ls application (print all files and folder in this folder).

> **os** library is your friend here, checkout it's documentation. ```import os```

1. make ls application that prints all files and folders in current folder
1. alter this implementation by accepting pathname as argument to your application

### Tick-Tack-Toe
Our first game! Let's make our first game with creating a tick-tack-toe game.

* 3x3 map will be used
* Two player hotseat game (players input after each other)
* User may select where they will put their mark
* After each input program will print out the current situation
* After each input program will make winner evaluation and declare winner and exit program if a winner is found.

#### Cheat of the day
*raw_input()* and *input()* functions are your friends here. With those you can capture
input from user while program is running.

```python
command = raw_input("Where do you want to tack?:")
```


