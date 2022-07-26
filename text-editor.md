# The Text Editor

**the comand line**
A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text
The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands. Here is an example:

```
ls -l /home/ryan
total 3
drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
```
## The Shell, Bash##
Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.

If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.

The terminal may seem daunting but don't fret. Linux is full of shortcuts to help make your life easier. You'll be introduced to several of them throughout this tutorial. Take note of them as not only do they make your life easier, they often also save you from making silly mistakes such as typos.

**Basic Navigation** 

*Introduction*

In this section, we'll learn the basics of moving around the system. Many tasks rely on being able to get to, or reference the correct location in the system. As such, this stuff really forms the foundation of being able to work effectively in Linux. Make sure you understand it well.
What's in Our Current Location?
It's one thing to know where we are. Next we'll want to know what is there. The command for this task is ls. It's short for list. Let's give it a go.

In the above example, the square brackets ( [ ] ) mean that those items are optional, we may run the command with or without them. In the terminal below I have run ls in a few different ways to demonstrate.

```ls
bin Documents public_html
ls -l
total 3
drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
ls /etc
a2ps.cfg aliases alsa.d cups fonts my.conf systemd
...
ls -l /etc
total 3
-rwxr-xr-x  2 root root 123 Mar 23 13:34 a2ps.cfg
-rwxr-xr-x 18 root root 78 Feb 17 09:12 aliases
drwxr-xr-x  2 ryan users 4096 May 05 17:25 alsa.d
...
```
Let's break it down:

Line 1 - We ran ls in it's most basic form. It listed the contents of our current directory.
Line 4 - We ran ls with a single command line option ( -l ) which indicates we are going to do a long listing. A long listing has the following:
First character indicates whether it is a normal file ( - ) or directory ( d )
Next 9 characters are permissions for the file or directory (we'll learn more about them in section 6).
The next field is the number of blocks (don't worry too much about this).
The next field is the owner of the file or directory (ryan in this case).
The next field is the group the file or directory belongs to (users in this case).
Following this is the file size.
Next up is the file modification time.
Finally we have the actual name of the file or directory.
Line 10 - We ran ls with a command line argument ( /etc ). When we do this it tells ls not to list our current directory but instead to list that directories contents.
Line 13 - We ran ls with both a command line option and argument. As such it did a long listing of the directory /etc.
Lines 12 and 18 just indicate that I have cut out some of the commands normal output for brevities sake. When you run the commands you will see a longer listing of files and directories.


***Paths***

Absolute and Relative Paths
There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.
