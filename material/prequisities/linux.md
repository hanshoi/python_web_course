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

**pwd** Tells where you are currently in as absolute path.

```bash
~$: pwd
/home/myusername/
```

####
