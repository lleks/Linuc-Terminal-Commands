# Linux-Terminal-Commands
List of frequently used Linux terminal commands


## Environment settings:
1. Download and install VirtualBox
2. Download Ubuntu
3. Select "New" tab in Virtual box, go  through
4. Install Ubuntu

### Open terminal (Windows):
`Ctrl + Alt + t`

### Close Terminal:
`Ctrl + d`

`exit`

### Open terminal (Mac):
`Ctrl + Option + t`

### Close Terminal:
`Ctrl + d`

`exit`

### Under which users terminal worked on:
`whoami`

### Print on the screen "Hello, World!":
`echo Hello, World!`

### Show current date:
`date`  long format

`date +%D`  mm/dd/ee

`cal` show month calendar (`sudo apt install ncal` - if command does not work)

`cal 2023`  calendar for 2023 year shown

`cal -y`  current year calendar shown

`cal 12 1987`	

### Combine command:
`echo "Hi dude, today is: $(date +%D)"`

### Present Working Directory:
`pwd`		print working directory

### Clears the terminal:
`clear`

`Ctrl + l`

### Changing Directories:
`cd /tem`	go to /tem directory

### Navigating to home directory:
`cd`

`cd ~`

`cd ~USENNAME`  go to USERNAME home directory

### Move to the root directory:
`cd /`

### Navigating through multiple directories:
`cd /dev/cpu`

### Moving up one directory level:
`cd ..`

### Moving back one previous level:
`cd -`

### Absolute Path (/home/guru99/Pictures):
`cd /home/guru99/Pictures`

### Listing files:
`ls`

`ls -R`			to shows all the fils les not only in directories but also subdirectories 

`ls *`			-//-

`ls -l`			detailed information of the files

`ls -a` 		hidden file shown

`ls -t`			sort by time and date

`ls -s`			size

`ls -la --color`	long format, hidden file, color text

`ls /usr`		listing of "usr" repository

Note:

Directories are denoted in blue color.

Files are denoted in white.

### Create a new file:
1. `cat > filename`
2. Add content
3. Press 'ctrl + d' to return to command prompt.

Or:

`touch filename`

Or:

`echo "some data" > filename`

### File type:
`file filename`

### What inside the file/ view a file:
`cat filename`

`less filename`		result per page shown (`q` for exit)

### Add text in file:
`cat >> filename`	

`vim filename`

### Combine 2 files in 1:
`cat file1 file2 > newfilename`

### Moving files:
`mv filename new_file_location`

(mv file1 /home/guru99/Documents)

### Renaming file:
`mv filename newfilename`

(mv file1 file3)

### Delete files:
`rm filename`

### Word counting in file:
`wc -w filename`

### Line countinf in file:
`wc -l filename`

### Characters counting in file:
`wc -c filename`

### Creating Directories:
`mkdir directoryname`

### Creating a "MUSIC" directory in a different location:
`mkdir /tmp/MUSIC`

### Removing Directories:
`rmdir directoryname` (for emptie directories)

`rm -r directoryname` (for not emptie directories)

### Renaming Directory:
`mv directoryname newdirectoryname`

### Calculate the size of a folder:
`du –sh FOLDER_NAME`

### Help on any command:
`man comandname`

`help COMMANDNAME`	if man does not work

`help`			list of available command for help	

### The History Command:
`history`

### Execute command #4 from history order:
`!4`

### Clean all history command:
`history -c; history -w`

### Command location:
`echo $PATH`	location of all programm shown

`which date`	location of "date" programm (command) shown

### Installing Software:
`sudo apt-get install packagename`

`sudo apt install PACKAGENAME`

### Updating all the installed packages
`sudo apt-get update`

### Changing file/directory permissions:
|User|Denotations|
|:---|:---:|
|u|user/owner|
|g|group|
|o|other|
|a|all|

### Absolute mode:
`chmod permissions filename`

|Number|Permission Type|Symbol|
|---|---|:---:|
|0|No Permission|---|
|1|Execute|--x|
|2|Write|-w-|
|3|Execute + Write|-wx|
|4|Read|r--|
|5|Read + Execute|r-x|
|6|Read + Write|rw-|
|7|Read + Write + Execute|rwx|

`chmod 764 file1`

Permission is shown as '-rwxrw-r--'

- Owner can read, write and execute
- Usergroup can read and write
- World can only read

### Symbolic Mode:
|Operator|Denotations|
|:---|:---|
|+|Adds a permission to a file or directory|
|-|Removes the permission|
|=|Sets the permission and overrides the permissions set earlier|

`chmod o=rwx file1`

Permission is shown as '-rwxrw-rwx'

### Changing Ownership:
`chown new_owner filename`

### Changing Ownership and Group:
`chown new_owner:new_group filename`

### Changing Group:
`chgrp new_droup_name filename`

### Output Redirection:
`ls -al > filename`			delete all previous contents of that file (ore craate new file if not exists besore)

`echo "some_text_here"> filename`		-//-

`ls -al >> filename` 			add more content to an existing file	

`echo "some_text_here" >> filename`	-//-

### Showing only one scroll length of content at a time:
`cat filename | less`

`cat filename | more`

### The 'grep' command:
`grep "search_string" FILENAME`

`cat filename | grep "search_string"`

`grep "search_string" filename > filename2`

|Option|Function|
|---|:---|
|-v|Shows all the lines that do not match the searched string|
|-c|Displays only the count of matching lines|
|-n|Shows the matching line and its number|
|-i|Match both (upper and lower) case|
|-l|Shows just the name of the file with the string|
|-w||
|--color||

`grep -iw error log.txt`

`cat filename | grep -i "search_string"`

### Display value of a Variable:
`echo $VARIABLE`

Set New Environment Variables:
`VARIABLE_NAME="variable_value"`

### Deleting Variables:
`unset variablename`

### All Environment Variables:
`env`

### Running a Foreground/Background process:
1.	Start the programm
2.	Press 'Ctrl+z'
3.	Type `bg` (send process to background)

or type `fg` (to containe process in terminal)

### Show all the running processes on the Linux machine:
`top`

`ps`

### Kill:
`kill PID_number_of_process`

### VIM Editing commands:

i 	- Insert at cursor (goes into insert mode)

a 	- Write after cursor (goes into insert mode)

A 	- Write at the end of line (goes into insert mode)

ESC 	- Terminate insert mode

u 	- Undo last change

U 	- Undo all changes to the entire line

o 	- Open a new line (goes into insert mode)

dd 	- Delete line

3dd 	- Delete 3 lines

D 	- Delete contents of line after the cursor

C 	- Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion

dw 	- Delete word

4dw 	- Delete 4 words

cw 	- Change word

x 	- Delete character at the cursor

r 	- Replace character

R 	- Overwrite characters from cursor onward

s 	- Substitute one character under cursor continue to insert

S 	- Substitute entire line and begin to insert at the beginning of the line

~ 	- Change case of individual character

### How to exit Vim:
`:x`		- save and exit

`:wq`		-//-

`Shift+zz`	-//-

`:w` 		- save changes

`:q`		- exit from Vim if nothing was changed

`:q!`		- exit Vim and discard any changes

### Shell Script:
1. Create a file using a vim editor. Name script file with extension .sh
2. Start the script with #!/bin/sh
3. Write some code (`ls -la` for example)
4. Save the script file as filename.sh
5. For executing the script type `bash filename.sh`

### Shell Variables script:
1. Create a file using a vim editor. Name script file with extension .sh
2.Write some script

`#!/bin/sh

echo "what is your name?"

read name

echo "How do you do, $name?"

read remark

echo "I am $remark too!"`

3. Save the script file as filename.sh
4. For executing the script type `bash filename.sh`

### Creating a User:
`sudo adduser username`

### Disabling account:
`sudo passwd -l username`

### Deleting account:
`sudo userdel -r username`

### Wiew the existing groups:
`groupmod Press Tab key twice`

### Adding users to the usergroups:
`sudo usermod -a -G GROUPNAME USERNAME`

### Removing a user from Usergroup:
`sudo deluser USER GROUPNAME`

### Check the memory status:
`free -m`	to display output in MB
`free -g`	to display output in GB

### Reboot Linux:
`sudo shutdown -r now`

`reboot`

`sudo shutdown -r +10`		reboot in 10 min

### Shutdown Linux:
`sudo shutdown now`

`reboot -p`

`sudo shutdown +15`						shutdown in 15 min

`sudo shutdown 13:10`						shutdown at 13:10

`sudo shutdown 15:30 "System will be shutdown at 15:30."`	message before shutdown at 15:10

### Shutdown cancel:
`sudo shutdown -c`

### Inner IP:
`nslookup localhost`

### Local IP:
`ip addr show`

### Outer IP:
`wget -qO- eth0.me`

### Instll terminal web browser:
`sudo apt install lynx`

`lynx goodle.com`	open google.com in console browser
