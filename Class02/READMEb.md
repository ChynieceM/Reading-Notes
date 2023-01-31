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

> **Important Concepts**
>
> pwd - print working directory "where we are currently"
>
> Is - list the contents of directory
>
> cd - change directories "more to another directory" 
>
> Relative Path - a file or directory location relative to where we are in the file system
>
> Absolute Path - a file or directory location in relation to the root of the file system



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

## More About Files

> **Important concepts** 
>
> Everything is a file even directories
>
> Files can have any extensions or none in Linux
>
> Beware of typos and case

Everything is a file 
* a text file, directory file, the keyboard is a file (the system only reads this), the monitor is a file (the system writes this only)

A file extensions is usually 2-4 chara & tells us what kind of file it is
* ex. file.exe
* file.txt
* file.png, file.gif etc

The system dertemines what kind of file in Windows but in *Linux it ignores the file type* but it looks inside the file to see what kind it is.
* you can name a file whatever in Linux and it'll still determine it as an image for example.

**File Command** file [path]
This can tells us what kind of file we have 

***Whenever we specify a file command line its actually as path*** 
* directories are just special type of file

###### These systems are case sensitive
* especially when referring to files, which is why it *is possible to have 2 + files* with the same name and DIFFERENT cases
* a space on a command line helps us seperate items and how we identify each command line argument
* for ex. Holiday Photos is sen as two command line arguments

**Quotes**
* use single or double quotes

**Escape Characters**
* use a backslash \ to escape or nullify the special meaning of a character 
* for example,  a space b/w holiday photos would normally have a special meaning to separate them as specific command line argumetns, but here holiday\photos removes it
**SHORTCUT** if you use tab completion previously the terminal will automitally escape any spaces

###### Hidden files & Directories 
* To create a hidden file or directory us the **Is** command but the file name or directory neeeds to begin with a . (dot) 
 (an ex. of this is config. files are hidden so they wont get in the way of a user's everyday tasks)
* To show contents of the directory and hidden files use **-a**










## Questions/ Things I want to know more about
How does the terminal help us with everyday tasks?
What is the purpose of the terminal in relation to a text editor?
