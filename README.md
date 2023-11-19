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
website](https://git-scm.com/downloads).

Unless you have other preferences, choose all the default options during the
installation.

NOTE:

When you open git bash, you will be dropped into a shell in your home
directory. For me, it says `myuser@machine MINGW64 ~`

NOTE:

The shell may be daunting at first, but remember that it is simply just another
type of file explorer. To see the folder that your shell is running in (i.e.
working directory), use the `pwd` command. To list the contents of the working
directory, run the `ls` command. And, if you would like to change your working
directory, you can call the `cd` command followed by the name of your target
working directory.

## Step 2: Use git bash to create a folder

To create a folder, use the `mkdir` command followed by the name of the folder.
``` 
mkdir repos 
```

Navigate to that newly created folder with the `cd` command.
``` 
cd repos
```

## Step 3: clone the repository from git.sdsurocketproject.org

To download code from other git users, use `git clone`. The act of downloading
a local copy of a code repository using this method is called "Cloning".

After creating and navigating to the `repos/` folder, look at your prompt. In
yellow text, you should see `~/repos`, which shows that your working directory
is currently `~/repos`. The tilde (`~`) symbol is your home directory. Run the
`pwd` command to see the path expanded, and remember to run the `ls` command if
you are not sure what is in the folder.

We will clone this project using HTTPS (If you have already set up SSH with
git, you likely already know what to do).

Go to the repository's homepage. In the top right corner, there is a blue
button that says "clone". Click it and copy the HTTPS URL.

Paste it into the command shown below:

``` 
git clone https://git.sdsurocketproject.org/avionics/intro-projects/software_intro_project_linked_lists.git
```

After running this command, git may ask you to enter your login credentials.
When you do so, git will begin downloading the repository into a new folder
titled `software_intro_project_linked_lists/` in the directory you are
currently in. Remember to run the `ls` command if you feel lost.

In the future, you will learn how to set up SSH with git. SSH is notably
simpler to use after the first setup. Try generating yourself an SSH key using
the `ssh-keygen` command. Doing this is NOT required.

## Step 4: make a branch with your name on it to edit changes on

when you default clone master will be copied by default. Master (or main) is
holy, it is the purest and best, only peer reviewed changes make it to master
as it is supposed to be clean, meaning no errors. The master for this branch is
considered clean, it will compile with zero changes. The code has purposefully
removed things, but it will compile.

**Please name the branch uniquely do no just past branch name**

``` git checkout -b chris-branch ```

also run:

``` git push --set-upstream origin chris-branch ```

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

``` git pull ```

this will synchronize your personal machine with remote. this is necessary
before pushs as it prevents merge conflicts from rearing themselves on remote
which are a pain and sometimes impossible if you are dealing with binaries or
hex files since it's no longer human readable.

Once that is done we need to see how things look on your machine run:

``` git status ```

if you have untracked changes they wil be red, if they are tracked they will be
green. Ideally, since you are only supposed to change linked_list.cpp that
should really only be the change that you need to commit. 

you'll see in red:

``` modified:file_name ```

go ahead and run 

``` git add linked_list.cpp ```

NOTE: tab complete means you dont need to list out the entire file

run git status again and it will be green since the changes are accounted for:

``` git status ```

next create a commit that describes your changes 

``` git commit` ```

Note: there are many ways to do this far better than above, but for starting
out this will work. Normally vim or nano would open and you ideally give a
succinct explanation of your changes.

now: 

``` git pull ```

``` git push ```

this will write all of your changes to the remote branch that is now available
to everyone to work on and run locally if they wish.

hint: while on your branch run:

``` git diff master ```

"q" to quit

to view how your branch differs from master, this is extremely helpful before
submitting your code for peer review. Don't look like an idiot, proofread your
changes. The reviewer will first go directly to the diff to evaluate your work.

Once you have completed this come talk to me! @chris

If you get stuck still come talk to me, this is incredibly important to know
for software.
