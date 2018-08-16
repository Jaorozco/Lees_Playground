## Notes on Command Line

[Ryan's Tutorial: Learning Linux](https://ryanstutorials.net/linuxtutorial/navigation.php)

#### Directory Commands:
- _**'pwd'**_ =  Print Working Directory  
- _**'cd /'**_ = Moves to the main directory  
- _**'~'**_ = _'tilde'_ is referencing it back to your home directory    
     _For example LeeRyans-MacBook-Pro:leeryansolomon = ~/Documents (where Documents is under the home directory)_  
- _**'.'**_ = Reference to your current driectory that you are in e.g. ./Documents. This helps in looking at other directories without going into them  
- _**'..'**_ = Reference to your parent directory. Can be used several times in a path to keep going up a directory  
#### List Command:
- _**'ls'**_ = Short list of all the files in the directory  
- _**'ls -l'**_ = Long list of all the files in the directory  
- _**'ls -a**_ = List all the hidden files too. Any files starting with a dot in front of it is a hidden file. 
- _**'Use single quotes ('') when trying to call a file with a name that has spaces. You can alos use the backslash (\) too**_ 
#### Refering to a Manual in Terminal:
- _**'man'**_ = provides manual pages for the command to lookup. Press **'q'** to quit  
- _**'man -k**_ = provides a key word search instead of user type the exact command. press **'n'** to find the next found item  
#### Making a Directory:
- _**'mkdir'**_ = short for Make Directory
- _**'mkdir -p'**_ = to make parent directories as needed
- _**'mkdir -v'**_ = makes directory and tells us what it is doing  
- _**'CHMOD 755'**_ = helps open a file if permissions are not allowed  
#### Creating an Emtpy file:
- _**'touch'**_ = creates an  empty file  
- **NOTE:** Using the **'-r'** option, which stands for recursive, we may copy directories. Recursive means that we want to look at a directory and all files and directories within it, and for subdirectories, go into them and do the same thing and keep doing this  
#### Copying a file or directory:
- _**'cp'**_ = stands for copy  
#### Moving a file:
- _**'mv'**_ = moves files from one directory to another  
#### Removing(deleting) a file or directory:
- _**'rm'**_ = removes file from directory  
- _**'rmdir'**_ = removes directory  
#### Wildcards:
- _**'*'**_ = represents zero or more characters  
- _**'?'**_ = represents a single character  
- _**'[] (represents a square block)'**_ = represents a range of character  
- _**'^'**_ = represents to exclude characters (Acts like a _'Not In'_ function)  
#### Permissions: 
- _**'r (read)'**_ = you may view to the contents of the file  
- _**'w (write)'**_ = you may change the content of the file  
- _**'x (execute)'**_ = you may execute or run the the file if it is a program or a script  

#### Viewing permissions (interpreeting it):
**When using the '_ls -l_' command the first 10 characters of the output will help you identify the permission**  
- **Example - _'-rwxr----x'_**  
    1. 
