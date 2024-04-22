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
`ps -A` OR `ps -e` will return all processes.
<br>
`ps aux` provides a detailed list of all processes in a user-oriented format, showing user ownership, memory and CPU usage, and other details.
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
<br>
`kill "processID"` is the default method of killing processes (kill signal 15).
<br>
`kill -9 "processID"` is the brute force kill and the absolute last resort, can produce zombies if you kill the parent process.

# Nginx script
## Change permissions to execute the file
`chmod +x file.txt`


`# !/bin/bash`

## update
echo updating...
`sudo apt update -y`
echo done!

## Avoid user input
sudo DEBIAN_FRONTEND=noninteractive apt upgrade -y

## upgrade
echo upgrade packages...
`sudo apt upgrade -y`
echo done!

## install nginx
echo installing nginx...
`sudo apt install nginx -y`
echo done!

## restart nginx
echo installing nginx...
`sudo systemctl restart nginx`
echo done!

## enable nginx
echo installing nginx...
`sudo systemctl enable nginx`
echo done!

## install js20
echo install js20 <br>
`curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
sudo apt-get install -y nodejs` <br>
echo done

## Check node version
echo check node js version <br>
`node -v` <br>
echo done!

## install app folder
cd app folder <br>
install npm <br>
npm start app.js <br>

## Copy the code of the app from a local machine to your EC2 instance.
`scp -i your_ssh_key.pem -r path/to/your/local/code ec2-user@your_ec2_public_ip:/path/on/ec2`

## Copy the code of the app to your EC2 instance using Github
Create a Git repository, upload the code of the app to the repository and then clone the repository to the EC2 instance.

## Run Node JS app in the background of the script.
`npm start app.js &`



## Exercise
1.	Print the top 2 lines of chicken-joke.txt to the screen.

`head -2 chicken-.joke.text`
2.	Use a command to print the bottom 2 lines of chicken-joke.txt to the screen.

`tail -2 chicken-joke.txt`

3.	Use a command to number the lines of chicken-joke.txt when it output the file to the screen.

`cat -n chicken-joke.txt`

4.	Use a command only print to the screen the lines of chicken-joke.txt which contain the keyword chicken.

`grep "chicken" chicken-joke.txt`

## Linux rules
- Do NOT hard code credentials
- A script needs to be tested on a FRESH ec2 instance, to ensure that it runs as designed.
- A script needs to be tested to see if it will run multiple times without causing an issue.