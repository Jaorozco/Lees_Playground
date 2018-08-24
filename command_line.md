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
-_**'ls -ld'**_ = View the permissions for a specific directory  
- _**'Use single quotes ('') when trying to call a file with a name that has spaces. You can alos use the backslash (\) too**_  

#### Refering to a Manual in Terminal:
- _**'man'**_ = provides manual pages for the command to lookup. Press **'q'** to quit  
- _**'man -k**_ = provides a key word search instead of user type the exact command. press **'n'** to find the next found item  

#### Making a Directory:
- _**'mkdir'**_ = short for Make Directory
- _**'mkdir -p'**_ = to make parent directories as needed
- _**'mkdir -v'**_ = makes directory and tells us what it is doing  

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
    1. The first character identifies the type. If it is a (-) then it is a normal file. If it is a (d) then it is a directory  
    2. The following next three characters represents the permissions of the owner. A letter represents the presence of a                        permission and a dash ( - ) represents the absence of a permission. In this example the owner has all permissions (read, write and execute)  
    3. The following 3 characters represent the permissions for the group. In this example the group has the ability to read but not write or execute. Note that the order of permissions is always read, then write then execute  
    4. Finally the last 3 characters represent the permissions for others (or everyone else). In this example they have the execute permission and nothing else  
    
#### Change Permissions: [GO BACK AND READ THE 'CHANGE PERMISSIONS' TUTORIAL]
- _**'CHMOD'**_ = To change permissions on a file or directory  
- _**'CHMOD 755'**_ = helps open a file if permissions are not allowed  

#### Filters:
_***'head'**_ = Program that prints the first so many lines of the file. (You can also specify how many lines you would like to see)  
_**'tail'**_ = Program that prints the last so many line of the file. (You can also specify how many lines you would like to see)  
_**'sort'**_ = It will sort an input. By default it will sort alphabetically. Refer to 'man' for additional sort commands  
_**'nl'**_ = Show the number of lines. (Note it does not account for line spaces)  
     - _Example_: "_**nl -s '. ' -w 10**_":The first one '-s' specifies what should be printed after the number while the second one '-w' specifies how much padding to put before the numbers  
- _**'wc'**_ = Stands for word count 
     _ _'wc -l'_ = will give the number of lines  
     - _'wc -w'_ = will give the number of words  
     - _'wc -c'_ = will give the number of characters  
- _**'cut'**_ = program to use if your content is separated into fields (columns) and you only want certain fields  
     - _Example_ : "_**cut -f 1 -d ' '**_": the separator character may be anything you like, for instance in a CSV file the separator is typically a comma ( , ). This is what the -d option does (we include the space within single quotes so it knows this is part of the argument). The -f option allows us to specify which field or fields we would like (if we wanted the second column we would simple type _**cut -f 1,2 -d ' '**_  
- _**'sed'**_ = stands for stream editor, it effectively allows us to do a search and replace on our data  
     - "_sed 's/oranges/bananas/g' test1.txt_" = In our test1.txt file the 'sed' command will search for oranges and replace it with bananas. The initial **'s'** stands for substitute and specifies the action to perform (there are others but for now we'll keep it simple). Then between the first and second slashes ( / ) we place what it is we are searching for. Then between the second and third slashes, what it is we wish to replace it with. The **'g'** at the end stands for global and is optional. If we omit it then it will only replace the first instance of search on each line. With the g option we will replace every instance of search that is on each line  
- _**'uniq'**_ = stands for unique and it removes duplicate lines from the data. (_LIMITATION: Lines have to be in the adjacent i.e. one after the other_)  
- _**'tac'**_ = it is 'cat' in reverse :smiley:  
- _**'awk'**_ = **[PLEASE READ BEFORE BOOTCAMP STARTS!!!!!!!]**  
- _**'diff'**_ = **[PLEASE READ BEFORE BOOTCAMP STARTS!!!!!!!]**  

#### Grep and regular expressions (in short know as 're'):
- _**'egrep'**_ = is a program that will search each line for a give set of data which contains a given set of pattern (_e.g. egrep 'orange' mysampledata.txt results in **Susy oranges 5 Terry oranges 9 Susy oranges 12**_)
- _**'egrep -n'**_ = in addition to providing the each line the data contains it also provide the line number (_e.g. egrep -n 'orange' mysampledata.txt results in **2:Susy oranges 5 5:Terry oranges 9 7:Susy oranges 12**_)
- _**'egrep -c'**_ = just provides the number of line it matched (_e.g. egrep -c 'orange' mysampledata.txt results in **3**-)

#### Regular Expression Overview:
- _**'. (dot)'**_ = a single character.  
- _**'?'**_ = the preceding character matches 0 or 1 times only.  
- _**'*'**_ = the preceding character matches 0 or more times.  
- _**'+'**_ = the preceding character matches 1 or more times.  
- _**'{n}'**_ = the preceding character matches exactly n times.  
- _**'{n,m}'**_ = the preceding character matches at least n times and not more than m times.  
- _**'[agd]'**_ = the character is one of those included within the square brackets.  
- _**'[^agd]'**_ = the character is not one of those included within the square brackets.  
- _**'[c-f]'**_ = the dash within the square brackets operates as a range. In this case it means either the letters c, d, e or f.  
- _**'()'**_ = allows us to group several characters to behave as one.  
- _**'| (pipe symbol)'**_ = the logical OR operation.  
- _**'^'**_ = matches the beginning of the line.  
- _**'$'**_ = matches the end of the line.  

#### Regular Expression examples:  
- to identify any line with two or more vowels in a row = _**egrep '[aeiou]{2,}' mysampledata.txt**_. 
- any line with a 2 on it which is not the end of the line. In this example the multiplier + applies to the . which is any character = _**egrep '2.+' mysampledata.txt**_. 
- the number 2 as the last character on the line = _**egrep '2$' mysampledata.txt**_. 
- each line which contains either 'is' or 'go' or 'or' = _**egrep 'or|is|go' mysampledata.txt**_. 
- to see orders for everyone who's name begins with A - K = _**egrep '^[A-K]' mysampledata.txt**_. 

#### Piping and Redirection. 
There are three data streams whenever we run a command on the command line. They are as follows:  
- _**STDIN (0)**_ = Standard Input data (data fed into the program). 
- _**STDOUT (1)**_ = Standard output (data printed by the program, defaults to Terminal). 
- _**STDERR (2)**_ = Standard error (for error messages, also defaults to Terminal). 

##### Example of Redirecting a file (I created an 'Examples folder on my work laptop'). 
- _**ls > myoutput**_ (_The greater than operator ( > ) indicates to the command line that we wish the programs output (or whatever it sends to STDOUT) to be saved in a file instead of printed to the screen_). 
- _**cat myoutput**_ = Shows what got saved in the myoutput file (_i.e. a listing of all the files in the 'examples' folder_). 
- _**(>>)**_ = When using the double greater you append an exisiting command to the myoutput file. (_e.g. 'wc -l test2.txt >> myoutput')_. 
- _**(<) less than operator**_ = we can send data the other way. 

#### Redirectig STDERR file. 
- _**STDERR**_ = is stream number 2 and we can use these numbers to identify these streams. 
- Example of using to redirect error = **'ls -l test1.txt abc.txt 2> error.txt'** --->>> **'cat error.txt'** (_NOTE: In order to redirect error you simply place the **'2'** before the **'(>)'** operator_). 
- Example of using command to save both normal output and error message in a single file. = **'ls -l test1.txt abc.txt > myoutput3 2>&1'** (_NOTE: This can be done by redirecting the STDERR stream to the STDOUT stream and redirecting STDOUT to a file. We redirect to a file first then redirect the error stream. We identify the redirection to a stream by placing an & in front of the stream number (otherwise it would redirect to a file called 1)_).  

#### Piping [Ryan's Tutorial on Piping](https://ryanstutorials.net/linuxtutorial/piping.php):  
Mechanism of sending data from one program to another. (_This is pretty much like slicing in Python_). Also click on the link above to look at some examples.   
Example = **ls | head -3 | tail -1 > myoutput4**.   

#### Process Management (Read this later). 

#### Bash Scripting. 
- **'#! (Shebang)'** = Tells the system that directly after it will be a path to the interpreter to be used
- **'which bash'** = TO find out what type of interperator to use (_e.g.'which bash'_)
- **Variables** =  
                   1. **'$0' - The name of the script**.  
                   2. **'$1 - $9' - Any command line arguments given to the script. $1 is the first argument, $2 the second and so                        on**.  
                   3. **'$#' - How many command line arguments were given to the script**.  
                   4. **'$ - All of the command line arguments'**  
- **Backticks** = Look at example 'backticks.sh'
- 
