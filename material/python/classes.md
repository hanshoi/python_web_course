## Classes ##

Classes, objects and instances are the backbone of Object Oriented Programming.
This is widely used in Python world, however Python doesn't require you to use them nor use OOP.
Regardless of this it is good to know how to use classes and what they look like.

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

### Object
Object is a instance of class. In following example *Point* is a class and *point1* and *point2* are objects of that class.

```python
class Point(object):
    pass

point1 = Point()
point2 = Point()
```

> You can think of Class like a template, that gets replicated multiple times into Objects.

Every object is a entity of it's own. This means that doing a comparison ```if point1 == point2:``` will
always be false. They have their own variables and they will work in different ways, this will become apparent
as we move forward.

### Attributes
You can define attributes into classes and objects.

```python
class Point(object):
    x = 0
    y = 0

point1 = Point()
point2 = Point()

point1.x = 5
print point1.x
print point2.x
```

Here we have defined 2 class level attributes *x* and *y*. However on object level we change value of x for point1.
This will make the x to 5 on point1 only, point2.x will remain as is.

#### Calling
Objects (holds true for modules as well) attributes and functions are called with a dot syntax. Like this:

```python
point1.point_attrubute
point1.point_function()  # calling a function of this object
```

### Class Functions
Classes can have their own functions as well.

```python
class Point(object):
    x = 0
    y = 0

    def sum(self):
        return x + y

    def add(self, num):
        return self.sum() + num

point1 = Point()
point1.x = 5
point1.y = 7

print point1.sum()
# >> 12
print point1.add(2)
# >> 14
```

As you notice from example above, functions in classes are similar to normal functions with couple of distinctions:
* They are defined within the class
* They always have parameter ```self``` as first parameter.
* They are called through the object of that class.

Normal class functions include ```self``` and are called through it's object. This means calling like ```Point.sum()```
would not work but calling through the object ```point1.sum()``` will work.

> There is couple execeptions to calling through the object -rule, namely ```classmethod```s and ```staticmethod```s, but those
> we will go through in Advanced section of our guide.

```self``` represents object itself (hence `self`) in funcions, this means if you want to call function or access attribute
of that specific object, you would use ```self```. ```self``` is the first parameter of class functions always, even though
none would otherwise be given, and when that function is called it isn't counted as a parameter.

### Constructor
In Python constructors are called ```__init__(self)```. Contructor is a function that is called when object is created.

```python
class Point(object):
    def __init__(self, x, y=0):
        self.x = x
        self.y = y

point1 = Point(5, 7)
point2 = Point(3)

print point1.x
# >>> 5
```

```__init__``` is called with the object creation parentheses and with ```self``` as first argument. Otherwise it follows normal
function parameter rules.

Notice that we don't need to define attributes on class level as we define them in contructor. Defining attributes can be done
anywhere in class, however some functions may need them so you need to make sure that they are defined before accessing them.
Defining attributes is a good practice, it's actually better than defining them on class level.

*General rule of thumb is to define mutable attributes in constructor and immutable on class level.*

> Python classes don't use destructors


### Excercises ###
#### Product Inventory
Create an application which manages an inventory of products. Create a product class which has a price, id, and quantity on hand.
Then create an inventory class which keeps track of various products and can sum up the inventory value.

Invetory class implements:
* add_products()
* sum_prices()

#### Refactor Tic-Tac-Toe
Take your Tic-Tac-Toe game from functions excercises and make it so that it uses classes instead of pure functions. This means that
at least GameBoard, Player will have their own classes.

#### Linked List
Make a [singly linked list](https://en.wikipedia.org/wiki/Linked_list#Singly_linked_list). This means that (without using lists or
other data containers) make a list where every link only knows it's value and next item on the list (if such exists).

Implement following classes:
* LinkedList
* Link

Implement following features to LinkedList:
* append(), add a new item to end of list
* len(), get amount of items in the list
* del(position), remove item in given position
* insert(position), add item into given position in list (0 == first, 1 == second). If position longer that there is items, then append it to end of list.

