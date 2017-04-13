## Classes ##

Classes, objects and instances are the backbone of Object Oriented Programming. This is widely used in Python world, however Python doesn't require you to use them nor use OOP. Regardless of this it is good to know how to use classes and what they look like.

Basic idea in classes is to make custom data containers with custom data handling functions.

```python
class Point(object):
    x = 0
    y = 0

    def __init__(self, x, y):
        self.x = x
        self.y = y

    def get_sum(self):
        return self.x + self.y

point = Point(5, 8)
print point.get_sum()
print point.x
```

> Many times classes can grow from simple data container and related functions into behemoths
> that encompass whole lot of code related to that data within the container. However this
> should be avoided and try to keep classes clean and concise.

### Class Definition
Class is defined by it's keyword variable ```class```, followed by class name (written in CamelCase) and then parentheses which
contain classes this is inherited from and lastly a : which indicates that we go into next block of code.

```python
class ClassName(object):
    pass
```

```object``` is base class for all classes in python, so if you don't have anything specific to inherit from, then use ```object```.

> Unlike function definitions Classes are read as whole when they are encountered. However class functions are not run,
> their definition is just taken into account and saved for future use.

### Excercises ###

