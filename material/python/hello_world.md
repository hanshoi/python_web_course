# Hello World
We are going to replicate the legendary programming excercise 'Hello World' while learning basics of python variables. 


## Python File
Remember from the last chapter that you can execute python files with following syntax:

```bash
 ~$: python hello_world.py
```

Python files are executed from top to down. You write commands that will follow specific syntax (text in certain format), that
has to be very specific. When these commands are read by computer it will do the actions described in them.

## print
Print is a command that will do as it says, print anything given to it into terminal. Like this:

```python
print "Hello World"
```

> Note that for strings (plain text), you need to encompass them with " or ' signs.

*Now try to make the excercise 1*

## Variable Assignment
Okay, now think that you would want to save something for usage later in your application. This can be done
with assigning that into a variable. This means that you give a variable (generally some word) a value (string, number, whatever).

Variable assignment is done like this:

```python
myvariable = "Hi Jim!"
```

Now you can use that variable later on, for instance for printing.

```python
myvariable = "Hi Jim!"
print myvariable
```

This application would print text "Hi Jim!" into terminal.

## Code Comments
Sometimes you need to write some comments in your code. You can do this by prepending # in front of your text and
python will ignore everything on that line after that.

```python
# full line comment
myvariable = "Hi Jim!"  # after a variable comment
```

Also multiple line comments are possible by using triple "  to encompass those lines.

```python
"""
This is a 
multi 
line 
comment
"""
```


## Excercises
### Make Hello World Application
Now it is time to combine what you have learned and make your very first application. 

* Make python file that will print "Hello World!" text into terminal

### Make Hello Variable Application
Replicate assignment from previous application with using variables instead of pure strings.

* have variable **hello_world** for text "Hello"
* print these
