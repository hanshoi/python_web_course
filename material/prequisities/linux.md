# Learning Linux
This chapter will ensure that you get started with linux on right path and learn all you
need to proceed with python web development. However as we ain't concentrating on linux
itself on this tutorial hence this will be quite simplified. You will however get going
with it and will learn as you go later on.

## What is Linux
Linux is a free operating system for your computer, just like Windows 8 or Mac OS X. 
What distinguishes Linux from the previously mentioned is that its open source, this means
that anyone can join in to develop Linux. This doesn't make it brittle however, as there
is literally thousands of volunteers working on it and everything goes through rigorous 
review and testing. This would make it in some cases even more reliable and robust than 
its propietary counter parts.

## Tutorial
As I don't go in details I will provide another one that will. In this chapter we will be
following tutorial made by Ryan Chadwick, buy him a beer if you ever meet him.

[Ryans Linux Tutorial](http://ryanstutorials.net/linuxtutorial/)

## Contents
Stuff that you will need to learn to effectively use linux. Yes, everything here is terminal 
based so prepare for some character based hacking.

When you open your shell you should see something like this at first.

```bash
~$:
```

This means that you are in your home folder and ready to start hacking. **~** there means 
directory path, in this case it is your current users home folder */home/myuser/*. Users
home folder is generally marked with sign *~* and it can be used in navigation as well, like 
```cd ~```. *$:* is general separators that shows the current line you are writing on.

## Directory Structure
In linux your directory structure is constructed as a tree. You will have your root folder 
(like a tree would have) and everything else is just folders within that root folder. 

Root folder is referenced with single **/** sign. This means that using ```cd /``` will get 
you into root folder. This is similar than jumping into home folder with sign *~*.

Generally when you are using directory paths in linux you are using them either absolutely
or relatively. Absolute path is prefixed with */* and relative is not. This means that if
you write ```cd /tmp``` you will end up in *tmp* folder in root folder, however if you 
write ```cd tmp``` you will end up in *tmp* folder within you current folder.

Basic shortcuts:

| Sign | Description |
| ---- | ----------- |
| /    | Root folder |
| ~    | Home folder |
| .    | Current folder | 
| ..   | Parent folder |

## Files
Some basic file types are following:

* basic file, ```readme.txt```
* folder, ```home```
* hidden file ```.hidden.txt```
* link, ```link_to_another_file```

As you notice they are quite indistinguishable from each other though they behave in different ways. 
For checking what file is of what type ```file``` command is your friend.

### Commands
Using linux is based on running several separate programs that do one thing (but do it well).
This means that the whole directory navigation consists of series of commands that are small
programs by themselves. This means that while you are in your terminal you will insert commands
like *ls*, *cd*, *pwd* and others to do what you want.

Invoking a command is as simple as writing it's name and hitting enter. Try this now, with command
*pwd*

> If you are unsure what a command does you can ask it what it does with *--help* option. Options 
> are additional arguments that you give for commands, like this ```pwd --help```. Options 
> are generally separated from other arguments with prefix *-* or *--*. *-* being used for shorthands
> and *--* used for the long name, like help can in many cases be written as *-?* as well.

> Other useful option that is implemented in almost every program ins *--version* that will tell
> what version of program you are using.


### Basic Navigation
You can't much do anything if you don't know where you are, where you are going and how to get 
there. Therefore first thing is to learn basic navigation in terminal.

##### pwd #####
Tells where you are currently in as absolute path.

```bash
~$: pwd
/home/myusername/
```

##### ls #####
List contents of this folder.

```bash
~$: ls
material  README.md
```

> Good to know options are **-a** that reveals hidden files, **-l** that gives files as a list
> and shows more information about them.

##### cd #####
Navigate to folder.

```bash
~$: cd /
/$:
```

> Remember shorthand **..** here. It will get you into the parent folder or as in many cases is the 
> case to previous folder. Use it like this ```cd ..``` or chain it like ```cd ../../somefolder```.


### File Manipulation ###
Create, Remove, Move and Copy files and folders.

#### mkdir
Make a directory.

```bash
~$: mkdir tmp
~$: ls 
material  README.md  tmp
```

> Notice that this is just a shorthand for **make directory**.

#### rmdir
Remove a dir.

```bash
~$: rmdir tmp
~$: ls 
material  README.md
```

> Care to gues what is **rmdir** a shorthand for?

#### touch
Make an empty file.

```bash
~$: touch tmpfile.txt
~$: ls 
material  README.md tmpfile.txt
```

#### cp
Copy file or directory.

```bash
~$: cp tmpfile.txt /tmp
~$: ls
material  README.md tmpfile.txt
~$: ls /tmp
tmpfile.txt
```

> Use option **-r** when copying folders.

#### mv
Move file or directory.

```bash
~$: mv tmpfile.txt material
~$: ls
material  README.md
~$: ls material
tmpfile.txt
```

> This command is used when you rename your files and folders as well.

#### rm
Remove files.

```bash
~$: rm material/tmpfile.txt
~$: ls material

```

> Use with option **-r** to remove folders as well.


### Editing Text
Editing text in shell can be used either with commands ```nano``` or ```vi```. 
Of these two I recommend nano as it is the simpler to master.

### View files

#### cat
Prints the whole file content into terminal.

```bash
~$: cat myfile.txt
I am some text
in this file.

```

> If you have a massive file that you need to browse and printing it in your terminal
> is not feasible, then please use ```less```, it is made for browsing huge files.

### Permissions

> You can check permissions and ownership with ```ls -l```

#### chmod
Change permissions of file or folder.

```bash
~$: chmod 777 tmpfile.txt
```

> There is generally three levels of users user, group, all and three levels of permissions
> read, write, execute. This are represented with the three numbers in *chmod* command. First
> digit being user, second group and final digit is permissions for all.

> Permission level is number from 0-7, 0 being nothing and 7 being everything. This comes
> from binary system and every permissions (r, w, x) is one binary number and any combination
> of them is two of them allowed. This means that 1 is execute only, 2 write only, 3 execute and write,
> 4 read only and so on..

#### chown 
Change owner for file or folder

```bash
~$: chown root:root tmpfile.txt
```

> Option <user>:<group> means just that, whos file it is an into whos group does it belong to.

### Grep and Regular Expression

#### grep
Find pattern in file or text stream.

```bash
~$: grep text myfile.txt 
I am some text
```

> Notice that by default grep returns the line your pattern matches to.

### Filtering

#### head
Show certain number of lines at begining of file.

```bash
~$: head -1 myfile.txt
I am some text
```

#### tail
Show certain number of lines from end of file.

```bash
~$: tail -2 myfile.txt
in this file.

```

### Misc

#### echo
Print given text

```bash
~$: echo "Hello world"
Hello world
```

#### wc
Gives the size of file

```bash
~$: wc myfile.txt
7
```

> Different options gives different possibilities for different data for the file.

### Sudo
On Linux you can use program called sudo to run commands as different user. This is mainly used
to run commands as root user to do actions that you wouldn't be normally allowed to do.

```bash
~$: sudo touch /tmpfile.txt
```

> You are not normally allowed to write files directly into computers root folder but with
> sudo command you can do it, if you have root password that is. Writing files into root
> folder is not however advisable and should almost never be done or necessary.

## Piping
In Linux you can use several commands in conjunction with each other. This is possible as 
they operate on philosophy of sreams. This means that when you are typing ```ls``` you are
actuall getting a stream of results not a bulk of results.

> If you have difficulty grasping what this means then imagine a man throwing apples at you 
> one after another. Now as he does that, it gives you options, you could grap them or 
> hit them with a baseball bat. This however would not be possible if he would haul the
> whole basket at you at once.

Piping in Linux is achieved with sign **|**, this takes results from previous command and pipes
them to second command, from left to right.

```bash
~$: ls | grep README
README.md
```

## Redirection
You can redirect output to some other places as well and not just to your console.
This is achieved with signs **>** and **>>**. 

**>** redirects output into new file and **>>** appends output into existing file.

```bash
~$: ls > myoutput.txt
~$: cat myoutput.txt
myoutput.txt
material
README.md
~$: wc -l myoutput.txt >> myoutput.txt
~$: cat myoutput.txt
myoutput.txt
material
README.md
3 myoutput.txt
```

## Scripting
Fine thing about Linux is that you can combine all of this commands into a single script.
This way you don't need to execute them all again and again. Check out tutorial below for
more scripting information.

[Ryans Bash Scripting Tutorial](http://ryanstutorials.net/bash-scripting-tutorial/)


## Installing 
Installing applications are done through package managers. These programs fetch information
from managed package repositories and then use that for installing them securely on your system.
This means for installing packages running command **apt-get install** is enough.

Basic command combinations for Debian based distros are following.

| Command | Description |
| ------- | ----------- |
| apt-get install <somepackage> | install a package, just change <somepackage> with your package and you are set |
| apt-cache search <something> | Searches for package called something from repository |
| apt-get update | update repository list, if there was updates for packages or such |
| apt-get upgrade | update all packages that are in need of upgrade, remember to run *update* first |


## Other Tutorials
* [Linux Survivals Tutorial](http://linuxsurvival.com/linux-tutorial-introduction/)
* [University of Surrey Tutorial](http://www.ee.surrey.ac.uk/Teaching/Unix/)
