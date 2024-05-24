# VI Editor Usage Guide
The VI editor is a powerful text editor available in UNIX and UNIX-like operating systems. This guide provides essential commands and tips for using the VI editor effectively.

## Basic Commands
### Opening a File
To open a file with VI editor:
```
vi file-name
```
### Inserting Text
To insert text:
```
Press i to enter insert mode.
Type your text.
```
### Changing Mode
To change from insert mode to command mode:
```
Press Esc.
```
### Deleting a Line
To delete an entire line:
```
Press dd in command (esc) mode.
```
### Undoing a Deletion
To undo the last deletion:
```
Press u in command mode.
```
### Adding a New Line
To add a new line below the current line:
```
Move the cursor to the end of the current line.
Press Esc to ensure you are in command mode.
Press o (lowercase letter 'o') to open a new line below and enter insert mode.
```
### Searching Text
To search for a word inside the VI editor:
```
Open the file with vi file-name.
Press Esc to ensure you are in command mode.
Type /word-name and press Enter. This will search for the specified word.
```
### Saving and Quitting
Save and Quit
To save changes and quit:
```
Press Shift + ZZ.
Or, type :wq! and press Enter.
```
### Quit Without Saving
To quit without saving changes:
```
Type :q! and press Enter.
```
## Summary of Commands
```
Open a file: vi file-name
Insert text: i (then type text)
Change mode: Esc
Delete a line: dd
Undo delete: u
Add new line below: Esc > o
Search for word: Esc > /word-name
Save and quit: Shift + ZZ or :wq!
Quit without saving: :q!
```
By following these commands and tips, we can effectively navigate and edit text using the VI editor.  
**[The End]**