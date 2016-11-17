# Conditionals

In python conditionals are just **if** command. With that you can do marvellous things, if you know what you are up to.

```python
if 1 == 1:
    print "Jihaa"
```

## Block of Code
Python differentiates a block of code with indenting (4 spaces). This means that every indent will be different block of code
and depending on how you get into that block code, it will execute it at once. Like this:

```python
if True:
    print "This is only executed if 'if' is valid conditional."
```

### pass
The official placeholder command of Python is called *pass*. pass doesn't do anything except takes space in your code. Why would you
then write something like this? Because if you go to block without any code (yet) Python will raise a syntax error. So until you get
your stuff done you can put *pass* there so that no error will be raised.

```python
if True:
   pass
```

## if
If is a command that if conditions are met you will go to that block of code.

```python
if 1 == 1:
    print "My first if conditional!"
```

> Note that if will validate also if no comparison operator is given. By default if conditional will evaluate
> stuff with values that ain't inherently negative as valid. Inherently negative values are (0, False, None, [], "", {}, and so on...)

## else
If *if*-conditional is not valid you can write *else*. This means that if *if* is not true you will go to else. Like this:

```python
if False == True:
    print "We will never get here!"
else:
    print "Wohooo! My first else."
```

## elif
Sometimes you wan't to have many conditionals before your else. You can have as many you want with elif. Like this:

```python
if False:
    print "not here.."
elif True == False:
    print "not here either :("
elif True == True:
    print "We ARE HERE!!!"
else:
    print "never reaching here.."
```

> In Python multiple elif commands are same as Switch conditional in other languages.

## Excercises:
Cheat of the Day:
```python
import sys

command_line_arguments = sys.argv
```

This snippet of code will load all commandline arguments into a Python list called *command_line_arguments*. This means
that if you call your file like this:

```bash
~$: python myfile.py 1 2 "12 asd 12"
```

You will have Python list ["myfile.py", 1, 2, "12 asd 12"] in your Python code. Notice that the files own name will be in the list as well.

### Print Given arguments ###

1. Using the cheat of the day. Make a file that prints all given arguments including filesname.
1. Alter this given script so that it will print all given arguments *without* the filename.
1. Alter file again so that it will print only the first value given.
1. Alter so that it will print only first one if it is a number (can be converted to int)
1. Test will your code work if you give no arguments? If not, fix this. (can break if wrong format)


### Calculator

Create a calculator application.

Make your calculator python file take in an mathematical operation and print out the correct answer.
You need to support at least following types of mathematical operations:

* add
* subtract (-)
* multiply
* divide
* modulo
