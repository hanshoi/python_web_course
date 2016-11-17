# Data Types

In Python there is different data types that you can use. Here are some examples what are data types:

* string
* boolean (True or False)
* numbers
* list
* dictionary
* or write your own

You can assign datatypes into variables in Python. In Python variables ain't statically typed, this means
that variables take any kind of datatype and you can't know what variables holds what type of variable.
*Python is built on trust*, this means that it is up to developers to decide what is what and trust that
others will do as agreed.

> **Python is built on trust**

## Converting Data Types
You can convert into any data type by calling that type name as a function, like this:

```python
myvar = int("10")
```

Code above will convert string "10" into integer number 10

> Of course you can't convert everything to anything, like string "AAA" just won't become a number.

## Basic Types

### bool
[Boolean](https://en.wikipedia.org/wiki/Boolean_algebra) is a value that can be either True or False and nothing else.

```python
myvar = True
myvar = False
myvar = bool(1)
```

### integer
Integer is your basic number, like 1, 2, 3 .... 121209312309. Integer is however always a non-decimal number.

```python
myvar = 1
myvar = 123213
myvar = 123123123
myvar = int(1.0)
```

> Note that the conversion example int(1.0) will convert it to a integer 1, as decimals ain't supported in this data type.

### float
Decimal number, like 1.1, 5.123123.

```python
myvar = 1.0
myvar = 0.000123
myvar = 1231.23123
myvar = float(2)
```

### string
Sting is you basic plain text 'word' that you use. You can use ' or " for marking strings.

```python
myvar = "some word"
myvar = "more words"
myvar = "c"
myvar = str(222)
myvar = """This is a
multiline
string"""
```

> You can use multiline strings by using """ """ notation (same as for multiline comment).

> Note that string only supports ASCII characters.

For more string operations please refer to Pythons own documentation [here](https://docs.python.org/2/library/string.html).

### None
None is the null variable of Python. This means empty variable. Variable with nothing in it.

```python
myvar = None
```

> You can't convert into None. Like True or False, None is always the one and only instance in Python,
> so some different rules apply. But more of this later.

## Container Types
Container types are those that contains other data.

### list
List is a basic list of things (variables). List is usually encompassed with square bracets [] and all variables are
separated with **,**. List is always mutable (you can change it's content) and ordered (items stays in order given).

```python
mylist = [1, 2, 3, "test", 1.1, True]
myvar = [1, 2, 1]
```

> In Python you don't need to have same variable type in your list. It is up to you what you have there.

#### append
You can add stuff into list by calling append function. Append always adds that item into last position of the list.

```python
mylist = [1, 2]
mylist.append(3)
```
Now you have list [1, 2, 3]

#### Access Position
You can access list by calling that position by it's index number in square brancets []. Index number is the
position of number in a list, note that numbering in programmin always starts from 0 not 1, meaning that first item
in list will be accessed with [0] not [1] (which will be the second item).

```python
mylist = [1, 2, 3]
print mylist[0]
```
This will print number 1 on the terminal.

#### pop
Will remove item on the list. On default the first one, but you can give it a index number as well.

```python
mylist = [1, 2, 3]
mylist.pop(0)
mylist.pop(1)
```

Now you have a list [2], can you explain why?

I won't go deeper into list here and now, if you need more check Python official documentation about it
[in here](https://docs.python.org/2/tutorial/datastructures.html).

### tuple
Same as list but is immutable (can't be changed once created). tuple is created with basic brancets ()


```python
mylist = (1, 2, 3, "test", 1.1, True)
myvar = (1, 2, 1)
```

Accessing is done same way as in the lists.

### dict
Dictionary is a container where you will assign your data with a keyword and can use that for searhing it quicly later on.
Dictionary is always unordered (order will change every time you call it) and mutable.

```python
mydict = {'key': 'value', False: 1.1}
myvar = {'somefloat': 1.1}
```

#### Accessing Data
You can access data by typing the keyword in squarebracets.

```python
mydict = {'key': 'value', False: 1.1}
mydict['key']
mydict[False]
```

### Add Data
You can add data by accessing with squarebrancets and new key and giving that a value.

```python
mydict = {'key': 'value', False: 1.1}
mydict['somekey'] = "some new value"
```

### Remove Data
You can remove data with the command *del*

```python
mydict = {'key': 'value', False: 1.1}
del mydict['key']
```


## Excercises
### Lists
1. make list with three integers
1. add number 4 into it
1. remove third number from it
1. make list of string
1. add that list into the integer list

### dictionary
1. make dict with three key-value pairs
1. add list into dict with number 1 in it
1. add dict into list
1. make second dict and add that into that list as well
1. now try to access the number 1 from the first list
