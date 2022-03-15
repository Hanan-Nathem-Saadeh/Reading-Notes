# Prep: Practice in the Terminal
# The Command Line
It is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.
---
## Opening a Terminal Steps:
If you are on Windows and intend to remotely log into another machine then you will need an SSH client. A rather good one is Putty (free) .

**(The Shell, Bash):
Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running
commands and the most common one is called bash.**
---
# Basic Navigation!
* pwd (Print Working Directory) -> tells you what your current or present working directory is.
* ls (List) -> know what is there.
* Absolute paths specify a location in relation to the root directory.they always begin with a forward slash ( / )
* Relative paths specify a location in relation to where we currently are in the system.
* cd -> Change Directories - ie. move to another directory.
* ls -a -> List the contents of a directory, including hidden files.
### Extra Knowledge -> some more building blocks to build paths:
* ~ (tilde) - This is a shortcut for your home directory.
* . (dot) - This is a reference to your current directory.
* .. (dotdot)- This is a reference to the parent directory.
---
# The Files :(everything is actually a file)
A file extension-> set of 2 - 4 characters after a full stop at the end of a file,some extensions:
   * file.exe - an executable file.
   * file.txt - a plain text file.
   * file.png, file.gif, file.jpg - an image.
## Notes:
- Linux is Case Sensitive.
- Spaces in file and directory names are perfectly valid but we need to be a little careful with them. 
- Anything inside quotes ``/"" is considered a single item.
- escape character( \ ) ->  escape (or nullify) the special meaning of the next character.
---
# Manual Pages
* man <command to look up> -> set of pages that explain every command available on your system including what they do.
* To exit the man pages press 'q'.
* man -k <search term> -> Do a keyword search for all manual pages containing the given search term.
* /<term> Within a manual page, perform a search for 'term'.
* n After performing a search within a manual page, select the next found item.
---
# File Manipulation:
  * mkdir -> Make Directory .
  * rmdir -> Remove Directory.
  * touch -> Create a blank file.
  * cp -> Copy file or directory.
  * mv -> Move file or directory (can also be used to rename).
  * rm -> Remove a file.
  ## [Cheatsheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
  
