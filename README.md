# Print The Node of a linked list

The goal of this project is to get everyone set up so they may compile and run
C++ code and implement a simple print statement. The required software is git
bash for handling the necessary git commands and for now Visual Studio 2017/19.
Normally, in a professional environment, there would be a *Makefile* that would
have instructions for the compiler to build everything in the project, this,
but we are going to learn with Visual Studio's GUI for now. This project is not
a test of whether you can code, but to try and give the best representation of
software development in a collaborative environment. The pull request and
related material will be covered in an Avionics meeting; it is really important
and must be explained in person. This project is relevant only to users of
modern Windows operating systems.

Note: This code is taken from Sarkar's COMPE260 class in data structures.

Required Software (Windows):

- Git Bash
- Visual Studio 

Git Bash is a Windows application providing a bash shell and git.

Visual Studio is an IDE for developing in a ton of languages from Microsoft.
I've taken C++ classes that use it as the preferred IDE.


## Step 1: install git bash

Step one is to install git bash from the [the git
website](https://git-scm.com/downloads)

When installing it is safe to choose all the default options. (unless you have
other preferences)

NOTE:

So when you open it you will be dropped into a shell in your home directory.
For me is says `myuser@machine MINGW64 ~`

NOTE:

A dollar sign ($) means the shell command is run as the normal user. A pound
sign (#) means the command is run with elevated privileges (as root or
administrator). Do not include either in the copy/paste

NOTE:

If we go ahead and run the list command "ls" it will print out the contents of
the directory, in windows I believe this is where our user folder is. If you
have a place where you normally have code you can go to it by using "cd" or
"change directory", to see where you are at in the filesystem you can also send
"pwd" which is path working directory. If none of that made sense, dont fret
it. 

## Step 2: using git bash create a repo's folder by typing in:

``` $mkdir repos ```

and 

``` $cd repos ```

## Step 3: clone the repository from git.sdsurocketproject.org

There should be a yellow part on the screen that say ~/repos that shows that
where you are at, it's to this folder we are going to be cloning our linked
list. There are two ways of cloning, ssh and https. For now will we use https,
but in the future most devs I have worked with use ssh due to how easy it is to
manage ssh keys on a machine and clone from their repos. 

Go to the repo's homepage and on the top right there is a blue button that says
clone, click it and copy the https url address option.

To clone the repo run:

``` $git clone
https://git.sdsurocketproject.org/avionics/intro-projects/software_intro_project_linked_lists.git
```

It may prompt for login credentials, enter those and it should start pulling
the code. It will place a folder in repos that is the name of the cloned repo.

For future reference try and use ssh keys, it's a lot more common and safer in
industry. Also doesn't ever make you login since verifcation is done through
key exchange.

## Step 4: make a branch with your name on it to edit changes on

when you default clone master will be copied by default. Master (or main) is
holy, it is the purest and best, only peer reviewed changes make it to master
as it is supposed to be clean, meaning no errors. The master for this branch is
considered clean, it will compile with zero changes. The code has purposefully
removed things, but it will compile.

**Please name the branch uniquely do no just past branch name**

``` $git checkout -b chris-branch ```

also run:

``` $git push --set-upstream origin chris-branch ```

it will let you know you have switched branches, now you can do your work and
it will NOT be captured on master until ready for review through a PR.  Once
you are done with your changes, you are going to take your personal changes and
push them to the repo. 

you are pushing the fact that there is a new branch onto the repo.

now while on your branch make your changes.

## Step 5: code

The task at hand: inside linked\_list.cpp there is a display function with two
lines of code missing, one is a print statement the other is a pointers
operation intended to "walk" the pointer down the list. To get an example of
how these pointers are used, please reference the other linked_list functions.
Notice the code should build right off the bat without any changes needed.

If you need any help please feel free to reach out to me on teams @chris

If people find this too difficult, I will be adding additional information. So
far this has been my experience in a software dev role. Typically, we are hired
and we work on existing infrastructure and we are asked to add features or code
to an already existing code base. This is why this project is structured like
this. The tasks here would describe your first day on the job as a developer.
Which is why I think all these things are mandatory to know before you put any
language on your resume. Knowing git is really a necessary skill for being a
dev.

## Step 6: push code to your branch Once you are done coding go ahead and run:

``` $git pull ```

this will synchronize your personal machine with remote. this is necessary
before pushs as it prevents merge conflicts from rearing themselves on remote
which are a pain and sometimes impossible if you are dealing with binaries or
hex files since it's no longer human readable.

Once that is done we need to see how things look on your machine run:

``` $git status ```

if you have untracked changes they wil be red, if they are tracked they will be
green. Ideally, since you are only supposed to change linked_list.cpp that
should really only be the change that you need to commit. 

you'll see in red:

``` modified:file_name ```

go ahead and run 

``` $git add linked_list.cpp ```

NOTE: tab complete means you dont need to list out the entire file

run git status again and it will be green since the changes are accounted for:

``` $git status ```

next create a commit that describes your changes 

``` $git commit` ```

Note: there are many ways to do this far better than above, but for starting
out this will work. Normally vim or nano would open and you ideally give a
succinct explanation of your changes.

now: 

``` $git pull ```

``` $git push ```

this will write all of your changes to the remote branch that is now available
to everyone to work on and run locally if they wish.

hint: while on your branch run:

``` $git diff master ```

"q" to quit

to view how your branch differs from master, this is extremely helpful before
submitting your code for peer review. Don't look like an idiot, proofread your
changes. The reviewer will first go directly to the diff to evaluate your work.

Once you have completed this come talk to me! @chris

If you get stuck still come talk to me, this is incredibly important to know
for software.
