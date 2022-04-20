# Lab Report 1

## Installing VS code

![image](VScode.png)

* First we need to install visual studio code
* Go to [https://code.visualstudio.com](https://code.visualstudio.com) to download and install


## Remotely connecting

* install openSSH
* lookup your account at [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php)
* open a terminal in VS code by doing Terminal -> New Terminal in the menu options

![image](p2NewTerminal.png)

* type in `ssh cs15lsp22zz@ieng6.ucsd.edu` 
* replace zz with your assigned user name (ie awo)
* say yes to all the prompts, enter password
* you're now connected!

## Run some commands
* here are some useful ones:
* `cd` will change directory
* `pwd` show the current directory
* `ls` will list the files in the current directory

* this is what it looks like (see below)

![image](p3RunCommands.png)

## Moving files with scp

* we can securely copy files from the client (local machine) to the server
* do the `exit` command to logout of the server
* now do `scp <fileName.extension> cs15lsp22zz@ieng6.ucsd.edu:~/`
* this securely copies the file to the server

![image](p4scp.png)

## Setting an SSH key

* typing our password all the time is annoying
* we can fix this with an SSH key, so we can login securely without needing to retype our password all the time
* on the client (local machine) for Windows do `ssh-keygen -t ed25519`
* save the key to the file `/Users/<user-name>/.ssh/id_rsa: /Users/<user-name>/.ssh/id_rsa`
* click enter on everything, don't type anything, being sure not to enter a passphrase
* you'll get a puzzle picture on the terminal
* two files, the public and private keys are stored on our local machine
* we need to copy the public key to the .ssh directory on our server account, here's how:
* login to the server and do `mkdir .ssh`, then `exit` to logout
* on the client, do `scp /Users/<user-name>/.ssh/id_ed25519.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys`
* we can now ssh login to the server and do scp all without a password!
* it will look like this:
![image](p5-SSH-key.png)

## Optimizing Remote Running
* let's get efficient! Here are some pro tips:
* you can use the up arrow to quickly access previous commands
* you can have more than one terminal open at a time!
* You can combine login and commands in one line, like so:
![image](p6ProTips.png)
* this allows us to login to the server, execute some operation, and logout all at once!

