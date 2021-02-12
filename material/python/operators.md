# Operators

## List of operators
| Sign | Description |
| ---- | ----------- |
| + | Add sign will add two values together |
| - | Minus sign will remove value from another value |
| * | multiply |
| / | divide |
| % | modulo |
| = | Equal sign is used for assignment |


## Add operator
Add operator is perhaps the most versatile of them all. This is because it works for big range of different types of variables.
As all operators work for integers, add will work for lists, dicts, strings and so on.

```python
newlist = [1, 2, 3] + [4, 5]
newint = 1 + 4
newstr = "Hello" + " " + "World!"
```

## Operator assignment
You can combine some operators with assignment as well. Like this:

```python
myint = 1
myint += 2
```
Now myint would be 3 as 1 + 2 = 3.

This works for other operators as well.

```python
myint = 3
myint *= 2
myint /= 2
myint -= 1
myint += 5
```

## Comparison Operators

| Sign | Description |
| ---- | ----------- |
| == | Equals to. Two types are of same value |
| != | Equals not. Two types are definitely not of save value |
| is | Values are same instance (not just same value) |
| is not | Definitely ain't same instance (though might be of same value) |
| < | less than |
| > | greater than |
| <= | less or equal than |
| >= | equal or greater than |
| in | value is in iterable |

Examples:

```python
if True == True:
    pass

if True != False:
    pass

if None is None:
    pass

if 1 is not None:
    pass

if 1 < 2:
    pass

if 2 > 1:
    pass

if 2 <= 2:
    pass

if 2 >= 1:
    pass

if 1 in [1, 2, 3]:
    pass
```

> All of these are valid cases.

# and or
You can use operators *and* and *or* to combine comparison operations. For and both operations have to be true, but for
or only other one need to be true.

```python
if 1 == 1 or 2 == 1:
    pass

if 1 == 1 and True == True:
    pass
```
