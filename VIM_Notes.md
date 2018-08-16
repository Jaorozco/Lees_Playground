## Notes on VIM
Three modes in VIM:    
- Normal  
- Insert  
- Visual  

## Commands in VIM 
#### Changes with parens, quotes or curley brackets:
- **CI)** = Change in parens    
- **CI"** = Change inside quotes  
- **CI}** = Change inside curly brackets  
- **DI)** = Delete inside brackets  
#### Navigation:
- **k** = acts like the _**upper**_ arrrow  
- **j** = acts like the _**down**_ arrow  
- **l** = acts like the _**right**_ arrow  
- **h** = acts like the _**left**_ arrow  
- **'^(caret)'** = moves the cursor to the beginning of the line  
- **'nG'** = moves to the nth line (e.g. 5G would move to the 5th line)  
- **'G'** = moves to the last line  
- **'w'** = moves to the beginnning of a word  
- **'nw'** = moves to the beginning of the nth word (e.g. 5w would move to the beginning of the 5th word)  
- **'b'** = moves to the beginning of the previous word  
- **'nb'** = moves back 'n' word  
- **'{'** = move backward one paragraph  
- **'}'** = move forward one paragraph  
#### Reading, Inserting, Appending, Saving & Exiting:
- **`ESC`** key to make sure you are in normal mode  
- **:q!** = quit VIM  
- **'x'** = delete a character under the cursor  
- **'i'** = insert some text. _'Move the cursor on top of the first character AFTER where the text is to be inserted._  
- **'a'** = append some text. _'Move the cursor to the first line that you need to append. It does not matter what character the cursor is in that line_  
- **:wq** = saves the file and then exits  
**'CAT'** = lets you views the contents of the file without being in the VIM interface  
#### Deleting:
**dw** = delete + motion (w). _'w = Until the the start if the next word, EXCLUDING its first character'_ 
**de** = delete + motion (e). _'e = To the end of the current word, INCLUDING the last character'_ 
**d$** = delete + motion ($). _'$ = To the end of the line, INCLUDING the last character'_  
  
