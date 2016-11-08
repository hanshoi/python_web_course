# Python

[Python](https://www.python.org/) is a programming language. As a programming language Python will interpret your commands
(*code you write*) for computer to handle. As Python belongs to a group called scripting languages, meaning languages that
doesn't require compiling, will it use it's own executable to run python code.

As we are using Python executable to interpret our code instead of compiling it into executable (like in C or C++),
does it make Python quite easily crosscompatible. Only thing you need is Python application to be installed on your
computer. Also Python doesn't run on virtual machine like Java but is built on top of C code, so no virtual machines
are necessary.

> Remember that Python is a scripting language and not compiled one. This means a slight performance drop, so sometimes
> you need to change into some compiled language (like C).

Python has been written simplicity and readibility in mind. Therefore it's pleasant to read and easier to understand, making
it very suitable for teaching basics of programming. Other uses for Python is:

* Prototyping, Python allows to make working applications quickly, this makes it good for prototyping
* web development, many times web applications ain't performance sensitive (no big algorithms or anything) so it's good to use there.

## Python Versions
Currently there is two versions of Python, 2 and 3. 3 being the future of Python and there is large scale adoption going on currently
and it most propably is the preferred version to use at the time when you are reading it. 3 is also the version that you should be learning.

However on this tutorial we will be using version 2. This is because almost all companies are still using version 2, and if you see
a job application where Python is mentioned then they mean Python 2 (however it is good to know about Python 3 to land the job like a boss).

Python 2 is still the one that is used everywhere and all libraries and applications are using it. At end of 2016 there still ain't all libraries
and tools converted to Python 3 yet.

## Install
On most systems python is pre-installed with the operating system and if you followed my guidance and isntalled Debian based Linux distibution,
then you have it installed. If you don't have it, please refer to link below:

* [Install Python](https://www.python.org/downloads/)

## Usage
Using python is relatively simple. You just invoke your Python file with the python interpreter.

```bash
~$: python mypythonfile.py
```
Now python interpreter will read every command written in that file and execute them (given that they have been written in Python syntax).
So if your file contains following text:

```python
print "Hello you delicious developer!"
```

now running this file with Python interpreter would provide following:
```bash
~$: python mypythonfile.py
Hello you delicious developer!
```


### Python shell
You can use Python as a shell as well. You can do this by invoking Python directly without any file as paremeter. In Python shell you can
write Python commands and code directly:


```bash
~$: python
>>>
```

## PyPi
Python Package Index in a centralized repository/index from where we can install all our Python based packages. This is a easy to use tool
for using Python packages in your system. This means that you don't need to manually download any zip packages and install them that way,
but can use a tool like *apt-get* or *homebrew* to install packages for Python.

You install packages in Python with tool called **pip**, pip installs, removes, updates and all other stuff required for package management.
If you are familiar with any other package management tool, then *pip* will feel very familiar to you. You use it like this:

```bash
~$: pip seacrch pudb
~$: pip install pudb
~$: pip uninstall pudb
```
