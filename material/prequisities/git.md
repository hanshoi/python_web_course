# GIT
## Introduction
You need to save your code somehow. You do it for you essays in school already, you have them in all kind of places. You have essay_final.txt
on you computer, essay_final_final.txt on your thumbdrive and essay_this_is_really_the_final_one.txt on your laptop. You see the problem here?

For programming, even more so than your essays, it's imperative to save your work. So why not use dropbox? Reason is that we don't just want to
save it, we want to control it specifically. We want to have several people to work on single files, we want to go back on changes done
on files and we want to have it all available now. This is where version control comes in.

Git does what every version control system does, it makes your code available on internet so you and your team mates or code comrades can access
it from everywhere. It also handles replication of code files into everyones computer and most importantly of all, controls codes versions.
Version control can be seen as having multiple parallel versions of same thing that are developed simultaneously. Having tools to merge these
into one working version and also to go forward and back in history of changes in file or files.

There is several version control systems but best (and most difficult to grasp) is [git](https://en.wikipedia.org/wiki/Git). Git might be
mind bogling at the beginning but when you graps how it works it will let you become the
[benevolent dictator](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life) of your code.

## Getting Started
### Install Git
For installing git on your preferred platform please refer to instructions found [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

### Create Github Account
This is not strictly speaking required, you will need some kind of server instance to operate git properly, meaning that code is replicated somewhere
where it can be accessed by everyone that requires access to it. This can be a basic server anywhere on internet or another ready made service like github
(bitbucket?). However github is the home of most open source project and thus will serve as the example on this tutorial.

[Signup to github](https://github.com/join?source=header-repo)

### Setup
Okay, you now have git freshly installed on your computer and I'm expecting it to be a UNIX based computer as previously suggested on this
tutorial, if not please refer elsewhere how to run git on Windows. Now open up your github account on browser and start a terminal session
on you computer.

1. create new repository on your github page
1. add a README file into it on generation time
1. after creation of repository, navigate to your repository page
1. find a green button on the right for cloning and downloading repository
  * choose the cloning url
1. now run the following in terminal for your new url
  * ```git clone <my repository url>```
1. now you have a fresh repository on your computer. Congratulations!

Now if you want to learn more about how to use github, please refer to [this guide](https://guides.github.com/activities/hello-world/) for a
simple tutorial.


## Tutorial
For this part of our practicing we have chosen tutorial by Roger Dudler, by him a beer if you meet him.

[Tutorial](http://rogerdudler.github.io/git-guide/)

## Commands
I'm providing the useful commands cheat sheet here. All commands start with the word **git** so that is the beginning so a basic git command
would be something around the following.

```bash
git init <url>
```

#### init
Initializes new git repository. Usually done on server side.

```bash
git init
```

#### clone
Clone existing repository into given path

```bash
git clone <url>
```

#### status
Check current status of your code.

```bash
git status
```

> Tells which code has been changed, which of them has been staged for commit and which haven't.

#### add
Add file to be staged for commit.

```bash
git add some_code_file.py
```

> Staging for commit means that next commit will include that file to be managed by git version control.

#### rm
Remove file from git version control.

```bash
git rm somefile.py
```

> Running standard ```rm``` from bash will remove the file but it won't remove it from git version control.
> This means that next time you pull or change your code that file will be back, unless you remove it with git.

#### mv
Move or rename files

```bash
git mv some_file.py new_file.py
```

#### commit
Commit staged changes. (This is basically same as save on your text editor)

```bash
git commit
git commit -m "my commit message"
git commit -a
```

> Remember you need to have some staged changes for this to have any effect. *-m* is a good option for this one,
> it will allow you to write your commit message on that same line. *-a* is handy as well, it will commit all
> changes in all files that are already under version control, with this you just need to be sure what you do,
> not recommended for newbies.

#### push
Push your commits to remote server

```bash
git push
git push --set-upstream origin master
```

> After a commit you changes only exist locally, with push they will go to remote server as well.

#### pull
Pull commits from remote server

```bash
git pull
git pull --rebase
```

> In case someone has made changes and pushed them to remote server, this will allow you to
> "download" them into your computer. *--rebase* option will use rebase -merging strategy
> when combining/merging commits together, check more of this on rebase command.

#### branch
Change or create a new branch

```bash
git branch
git branch new_branch_name
```

> Without any argument it will list locally available branches (those you have pulled already).
> With argument it will create a new branch with that name.

#### checkout
Change branch to another one.

```bash
git checkout master
git checkout -b new_branch
```

> *-b* option allows you to create branch and checkout into it.


#### log
Commit logs

```bash
git log
```

#### reset
Discard uncommitted changes

```bash
git reset --hard
```

#### revert
Revert an commit

```bash
git revert <commit hash id>
```

> useful when you made something stupid in your commit

#### diff
Compare two versions and check the difference between them

```bash
git diff another_branch
git diff antoher_branch some_file.py
```

> You can limit the scope of diff command to some specific files or folders.

#### merge
Combine changes in two branches

```bash
git merge another_branch
```

> merge will take changes from branch given as argument and put them into your current brach.
> There may come some conflicts while you do this. Therefore it's good to know what you are
> doing.

#### rebase
Combine changes in two branches. Okay, this is same as merge right? No, not quite. Merge will
take another branch and merge changes there into this one. Rebase will take the whole branch
with history and all and make them into one linear path, like the other branch never would have
existed at all.

```bash
git rebase another_branch
```

> This is quite handy when combined with ```git pull``` command.

#### tag
Tag your commit with a meaningful name

```bash
git tag <a human readable commit name>
```

> Useful if you have some special point in code. Then give it a meaningful name with tag and
> you won't need to remember it's commit hash. This could be a release version number for instance.

#### stash
Put your code aside for a moment and do something else.

```bash
git stash
git stash list
git stash pop
```

> Handy when you need to change branch ASAP but you have just some scribles on your current branch, really
> nothing commit worthy.

## Handy Tools

* [gitk](https://git-scm.com/docs/gitk)
* [git-up](https://pypi.python.org/pypi/git-up)

## Pull Request
When using a external tool like github, you can make pullrequests. This is a feature where you have made a branch
or a fork of the main repo, made some changes there and you want to have those changes merged back to upstream
(the master branch). On a case like this, you would make a pull request.

Pull request is made so that another person can review your code and then either accept it or make some demands
on what you have made and ask for some changes, or if a specially nasty bugger, decline your changes outright.


## Excercises

### Configure your git ###

1. add email to git config
1. add username to git config
1. add couple of aliases to git config
1. set git to user rebase as default merging strategy
  * autosetuprebase = always
1. add these aliases
  * pushnew = "!s() { git push --set-upstream origin \`git rev-parse --abbrev-ref HEAD\`;  }; s"
  * l = log --oneline --decorate

### Make Your Own Repo
1. Make public github repo for excercises of this course
1. clone it to your computer
1. make 'develop' branch in it
1. checkout into it
1. Add a README.md file and some description in it (in markdown format)
1. commit and push
1. change to master
1. merge changes from develop branch and push
1. Return to develop and alter you README file.
1. Make a Pull Request in github from develop to master.
1. Comment your fancy README file in it and merge it.
1. return to master branch in terminal and pull your changes

### Clone Django
1. Search github for Django project
1. Clone it to your computer
1. change to release 1.7 branch
1. browse code around a bit
1. try to merge 1.8 branch into 1.7
  * run ```git merge --abort``` in horrific panic
1. return to master branch
