# Linux guide

## What is Linux?
Linux is open-source, with many distributions (so it’s very customidable).
<br>
- Works with Unix at a kernel stage.
<br>
- No GUI so you can access commands very easily as it is a CLI (command line interface).
<br>
- Tends to be faster as a result of this.
<br>
- Large community
<br>
- Cost effective
<br>
- Stable
<br>
- Big knowledge base
<br>
- Very employable skill
<br>
- Linux is case sensitive

## Commands
`uname` says what OS you're using.
<br>
`uname –help` shows all the things you can see for the specific command.
<br>
`whoami` shows who you're logged in as.
<br>
`cat` shows the contents of the file.
<br>
`cat /etc/shells` shows where all your shells are.
<br>
`ps -p $$` shows all the processes which are running.
<br>
`-p`: This option specifies the PID(s) of the processes to be displayed. 
<br>
`$$`: In Unix-like shells, $$ represents the PID of the current shell.
<br>
`history` shows all the commands you have run, up until the 500th.
<br>
`history -c` clears your history.
<br>
`curl` is used to transfer data.
<br>
`file cat.jpg` shows data of file.
<br>
`mv cat.jpg cat` renames file from cat.jpg to cat. The contents of the file remain the same, no matter the extension.
<br>
`cp` copies the file.
<br>
`cp cat cat.jpg` copies the file cat and creates a new one called cat.jpg.
<br>
`Rm cat` removes file.
<br>
`mkdir` creates directory.
<br>
`rm -r` is how you delete folders, -r means recursive.
<br>
`rm -rf` is how you force delete things.
<br>
`Touch` creates a file.
<br>
`nanome` allows you to edit the file.
<br>
`tree` shows files and directories, colour coded.
<br>
`mv file.txt destination` moves a file to the destination specified.
<br>
`chmod +x file.txt` gives permission to execute the file.
<br>
`sudo systemctl enable nginx` automatically starts nginx when the system turns on.
<br>
`nano .bashrc` to enter the .bashrc file.
<br>
`export variable=variable name` at the bottom of the .bashrc file to script the variable.
<br>
`source .bashrc` to run the script and substantiate the variable.

## Nginx script
`!/bin/bash`

## update
`sudo apt update -y`

## upgrade
`sudo apt upgrade -y`

## install nginx
`sudo apt install nginx -y`

## restart nginx
`sudo systemctl restart nginx`

## enable nginx
`sudo systemctl enable nginx`


## Exercise
1.	Print the top 2 lines of chicken-joke.txt to the screen.

`head -2 chicken-.joke.text`
2.	Use a command to print the bottom 2 lines of chicken-joke.txt to the screen.

`tail -2 chicken-joke.txt`

3.	Use a command to number the lines of chicken-joke.txt when it output the file to the screen.

`cat -n chicken-joke.txt`

4.	Use a command only print to the screen the lines of chicken-joke.txt which contain the keyword chicken.

`grep "chicken" chicken-joke.txt`

