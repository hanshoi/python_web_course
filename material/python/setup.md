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

Python has been written simplicity and readability in mind. Therefore it's pleasant to read and easier to understand, making
it very suitable for teaching basics of programming. Other uses for Python is:

* Prototyping, Python allows to make working applications quickly, this makes it good for prototyping
* web development, many times web applications ain't performance sensitive (no big algorithms or anything) so it's good to use there.

## Python Versions
Currently there is two versions of Python, 2 and 3. 3 being the future of Python and there is large scale adoption going on currently
and it most probably is the preferred version to use at the time when you are reading it. 3 is also the version that you should be learning.

However on this tutorial we will be using version 2. This is because almost all companies are still using version 2, and if you see
a job application where Python is mentioned then they mean Python 2 (however it is good to know about Python 3 to land the job like a boss).

Python 2 is still the one that is used everywhere and all libraries and applications are using it. At end of 2016 there still ain't all libraries
and tools converted to Python 3 yet.

## Install
On most systems python is pre-installed with the operating system and if you followed my guidance and installed Debian based Linux distribution,
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
You can use Python as a shell as well. You can do this by invoking Python directly without any file as parameter. In Python shell you can
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
~$: pip search pudb
~$: pip install pudb
~$: pip install setuptools --upgrade
~$: pip install flask==4.7.2
~$: pip install -r requirements_file.txt
~$: pip uninstall pudb
```
> *--upgrade* option will install the latest version of that package. This is the default behaviour when installing new packages but if you
> want to upgrade existing packages then that command is the way to go.

> Giving flask==4.7.2 will install specific version of that package. This a critical feature when programming as a profession. If you
> give program a general dependency to some package and some user will try to install you software 5 years later, do you think your
> code will be compatible still with the newest versions of packages you are using? Probably not..

> You can also put your dependencies into file (like *requirements_file.txt*) and then use option *-r* to install them from there.
> In conjunction of specifying package versions, this is the professional way to go.

All packages you install this way will require *sudo* prefix before them. This means that you are installing all those packages on system level.
As you are developing multiple projects and having literally hundreds of python packages that you need to install and there may be conflicts in
version dependencies as well, then this might not be the best way to go.

## Virtualenv
Virtualenv will create a sandbox for your python and python packages. This means that when you start a project and activate virtualenv, then
that python and pip will be from that virtualenv and not from system. This also goes for all packages that you install, this way all
packages you need for your project are neatly compartmentalized in their own places.

### Install
Only run following command:

```bash
~$: pip install virtualenv
```

or refer to their [installation documentation](https://virtualenv.pypa.io/en/stable/installation/).

### Usage
####create
When using virtualenv you will create new virtualenv with on of the following commands:

```bash
~$: virtualenv <name>
~$: virtualenv <name> -p /usr/bin/python2.7
```

just change *<name>* with something of you preference.

> *-p* option allows you to specifically define which python executable should be used as the base
> for this virtualenv.


####activate
Activate it by:

```bash
~$: source <name>/bin/activate
(<name>) ~$:
```

####deactivate
To stop using virtualenv.

```bash
(<name>) ~$: deactivate
~$:
```

## Virtualenv Wrapper (optional)
Okay, virtualenv is handy tool. However now you have folder everywhere with python packages in them and you need to remember which is where and
from where to run the ```source <name>/bin/activate``` from. This all doesn't quite sit with my engineering (lazy ass) sprit of mine. In come
virtualenvwrapper, it will handle all of this for you and provide easy to use commands for managing different virtualenvs.

Install it by running:

```bash
~$: pip install virtualenvwrapper
```

and add following lines in your *~/.bashrc* file.

```bash
export WORKON_HOME=$HOME/.virtualenvs
source /usr/local/bin/virtualenvwrapper.sh
```

now startup a new terminal session and you should have all the virtualenvwrapper commands available and all you virtualenvs will end up in one specific
folder *~/.virtualenvs*

#### mkvirtualenv
Create new virtualenv.

```bash
~$: mkvirtualenv <name>
~$: mkvirtualenv <name> -p /usr/bin/python3
```

> *-p* option specifies specific python executable to be used.

#### lsvirtualenv
List all currently available virtualenvironments.

```bash
~$: lsvirtualenv
<name>
=======
```

#### workon
Activate virtualenv with name

```bash
~$: workon <name>
(<name>) ~$:
```

#### deactivate
Deactivate current virtualenv

```bash
(<name>) ~$: deactivate
~$:
```

> Not a command from virtualewrapper but good to remember anyway.

## Misc (optional)
For the really lazy out there checkout following

* [autoenv](https://github.com/kennethreitz/autoenv)

This will automatize your ```workon <name>``` commands and save you from typing.
