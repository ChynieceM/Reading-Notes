## The Command Line

**GUI** = Graphical User Interface
* system of visual components for computer software
* GUIs display objects - information & represents actions that can be taken.
* Objects change color, size, or visibility when interacted with 

###### **The Command Line** aka *terminal*

Most people use the terminal interface as another window on their desktop

* The terminal is a text based interface to the system. 
* Enter commands and feedback will be given
* terminal presents you with a prompt 
* you also have **command line arguments** which are separated by spaces; there must be a space b/w the *command* and *1st command line* argument
* Most commands produce an output, other commands just perform tasks and dont show info unless theres an eror

###### The Shell Bash

The **Shell** is w/in the terminal. 
* This inicates how the terminal will behave and looks after running commands
* To know what shell you're using you can use the ***echo*** command to show the current shell -- as long as it shows something that ends in bash, its all good

**Shortcuts** 
1. Commands are stored in a history. So instead of re-typing, hit up arrow a few times



## Basic Navigation

**PWD** command aka *Print Working Directory* - where we at 

* PWD  tell you where your present working directory is 
* it helps you understand where you are if you get lost on the terminal

**Is** command - list of content in directory 

* This tells you what is there, lists your location
* how to use it -(no space in brackets) Is [ options ] [ location ] - the brackets means that those things are optional 
* using -1 means a **long listing** of contents of current directory

**Long Listing contains**: (Navigation)[https://ryanstutorials.net/linuxtutorial/navigation.php]

*These are all on one line*

1. 1st character shows normal file (-) or directory (d)
2. next 9 char are permissions for (-) or (d)
3. next is # of blocks
4. next is owner of file or directory
5. next is the group the file or dir belongs to ( for ex. users)
6. file size
7. modification time
8. actual name of (-) or (d)

##### Paths

When referring to a file or directory we are referring to the path 

**Path** a means to get to a file or directory 

**Absolute VS Relative Paths** 

The file system in linux is hierarchical
*at the top is the **root** directory. 
*the root is shown by one slash / 

*Absolute* paths specify a location relative to the root directory or whats at the top - always starts w/ forwrd slash /
*Relative* paths specify a location relative to where we are in the system - these dont start w a slash

Bulding Paths
~(tilde) home directory shortcut
.(dot) refers to current directory
..(dotdot) refers to parent directory

##### Change Directory

cd aka Change Directory
We use the change directory to move around in the system

ex. cd[change location]
* the cd command can be run w/out a location but usually is ran w/ 1 command line argument telling you where the location you want to change to 

Tab Completion - Hitting the tab button can invoke auto complete 

## About Files