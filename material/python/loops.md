# Loops #

When you want to do actions to all items in a list or just make a virtual hamster wheel, you
will need to use loops. Loop will do certain block of commands in a loop or cyckle.

## for
For loop will go through an iterable and run actions for every item in it.

```python
mylist = [1, 2, 3, 4]

for number in mylist:
    print number
```

Code above will loop through list *mylist* and print every number in it.

For loops are handy when you want to do actions to some set of items in list, tuple or dictionary or for other sets with finite number of items, like a range of numbers.

### tuples

#### Extract a tuple
You can extract values of tuple into variables by simple assignment. This means that if you have a tuple with three values you can assign it into three variables like this:

```python
id, name, title = (1, "Henry", "CTO")
```

> If you write code like above and for some reason there isn't three values in the tuple will Python throw an error.

#### looping list of tuples
You use variable extraction if for loops as well. Like this:

```python
mylist = [(1, "Henry"), (2, "Alex"), (False, "Nobody")]

for id, name in mylist:
    print id, name
```

> Note that print can also take several variables.

### Loop a dict
When looping a dict you can't just loop it through. You have to call some of it's helper functions to get it into iterable format. These are keys(), values(), items().

| name | description |
| ---- | ----------- |
| keys | will return a list of dictionary keys only |
| values | will return a list of dictionary values only |
| items | will return a list of tuples like this (key, value) |

```python
mydict = {'key': 1, 'somekey': False}

for key, value in mydict.items():
    print "{}: {}".format(key, value)
```

### range
Python built in command *range()* will give you a list with number from that given range.

```python
print range(5)  # 0-4
print range(2, 5)  # 2-4

for number in range(5):
    print number
```

## while
If you just want to keep looping until some condition is met, then use the while loop. While loop will keep looping until the condition given will be False. Condition is given in same way as in if-conditional.

This is a great way to create mainloops for instance (used in game engines and some applications).

```python

while True:
    print "Will never stop rocking!"
```

> Loop above will never exit as it is always True (unless an error is thrown).

## continue
*continue* command will skip all other commands in the code block and continue to next loop.

```python
mylist = [1, 2, 3, 4]

for number in mylist:
    if number == 3:
        continue
    print number
```

Code above will never print number 3.

## break
*break* command will stop looping completely.

```python
mylist = [1, 2, 3, 4]

for number in mylist:
    if number == 2:
        break
    print number
```
Only number 1 will get printed.

## Excercises

### FizzBuzz
Lets do this classic programming excecise. Print all number from 0 to 100. If number is divisible with 3 then print "Fizz" instead of the number, if the number is divisible with 5 then print "Buzz", if it is divisible with both then print "Fizz Buzz".

### ls
Make your own ls application (print all files and folder in this folder).

> **os** library is your friend here, checkout it's documentation. ```import os```

1. make ls application that prints all files and folders in current folder
1. alter this implementation by accepting pathname as argument to your application

### Palindrome
Checks if the string entered by the user is a palindrome and print out if it is.
That is that it reads the same forwards as backwards like “racecar”


