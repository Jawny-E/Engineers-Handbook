
**Table of Contents**

- [[#Shell Scripting|Shell Scripting]]
	- [[#Shell Scripting#The kernel|The kernel]]
	- [[#Shell Scripting#The shell|The shell]]
		- [[#The shell#Command Line Shell|Command Line Shell]]
		- [[#The shell#Graphical Shell|Graphical Shell]]
	- [[#Shell Scripting#The terminal|The terminal]]
	- [[#Shell Scripting#Shell Scripting|Shell Scripting]]
- [[#Bash Scripting|Bash Scripting]]
- [[#Networking|Networking]]
- [[#Security Tips|Security Tips]]
- [[#Linux Containers|Linux Containers]]
- [[#Operating system|Operating system]]

## Commands I've used

| Command          | Short                                                        |
| ---------------- | ------------------------------------------------------------ |
| ls               | Check content of a folder                                    |
| cd               | Change Directory<br>                                         |
| man              | Manual for other commands                                    |
| mv               | Move or rename a file                                        |
| mkdir            | Make a new directory                                         |
| rmdir            | Remove directory                                             |
| rm               | Remove a specific file                                       |
| cat              | View the contents of a file                                  |
| pwd              | Check current working directory                              |
| touch            | Used to create a file                                        |
| chmod            | Used to change the access mode of a file                     |
| nano             | Used to edit a file                                          |
| rm -r nameOfDir/ | Delete entire directory and its contents                     |
| code             | Used to open the given directory and its contents in VS Code |
| ssh              | Securely connect to a remote server                          |
| eval ´ssh-agent´ | Starts the ssh-agent                                         |
| ssh-keygen       | Create a private and a public key-pair                       |
| ssh-add          | Add an ssh key to the given path                             |
| hostname -I      | Check local IP-address quick                                 |
| ip addr          | Check IP-addresses more thoroughly                           |
| head             | Shows first lines of a file                                  |
| tail             | Shows last lines of a file                                   |
| uname            | Print system info                                            |
| whoami           | Display current username                                     |
| uptime           | See system uptime                                            |

### Git and Commands

| Command           | Short                                                                                 |
| ----------------- | ------------------------------------------------------------------------------------- |
| git log (-p -2)   | Shows the git log, the info in the parenthesis gives the last 2 logs                  |
| git status        | Shows the current state of your repository, including tracked and and untracked files |
| git push          | Pushes local commits to the remote repository                                         |
| git branch (-a)   | Lists all branches in this repository or all remote and local branches                |
| git diff          | Shows changes between the working dir and he staging area                             |
| git checkout (-b) | Creates a new branch, add -b to switch to said branch as well                         |
| git commit -m     | Creates a new commit with the changes in the **staging area**                         |
| git add           | Adds a file to the **staging area**                                                   |
| git show          | Shows the details of a specific commit                                                |
| git fetch         | Retrieves changes from a remote repository                                            |
| git pull          | Same as fetch, but also merges them into the current branch                           |
==git push --set-upstream origin name_of_branch==

Pull requests - asking for your branch to be merged with main

## Shell Scripting
### The kernel
The kernel is the core of the operating system. On Linux the Kernel manages the following resources:
- File management
- Process management
- I/O management
- Memory management
- Device management 
- etc
### The shell
The shell is a user program that interfaces the user with operating system services. It takes commands readable by humans and converts them into something the kernel can understand. There are broadly two categories of shell:
#### Command Line Shell
One can access the shell through the command line interface. This is a special program called Terminal or Command Prompt in the largest OS-types. Here a human can type in a readable command such as **cat** and then the results are returned such as shown in the image below
![[TERMINAL2.png]]
#### Graphical Shell
Graphical shells lets the user manipulate programs through a Graphical User Interface GUI. These operations can be opening, closing and moving windows. 

### The terminal
The terminal is the program responsible for interfacing a user with the shell

### Shell Scripting
Is the act of stringing a bunch of shell commands together so that we can avoid manually typing them out. They are made in files with the .sh extension, and uses syntax like most other programming languages. 
- Shell Keywords - if, else, break
- Shell commands - cd, ls, echo, pwd
- Functions
- Control flow
One can find pretty good tutorials on howto make and use shell script
## Bash Scripting
Is for many purposes  just an extension of Shell Scripting. It is a command-line interpreter or Unix Shell used in GNU/Linux Operating System.

It supports variables conditional statements, and loops just like programming languages. 

## Networking


## Security Tips 


## Linux Containers


## Operating system

