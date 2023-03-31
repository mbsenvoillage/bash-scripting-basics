# Lesson 2: Basic Syntax and Commands

## The Bash command line

The Bash command line is the interface through which you can interact with the shell. It allows you to enter commands and receive output from the shell. To access the command line, open a terminal or command prompt and type bash.

## Running commands and getting output

To run a command in Bash, simply type the name of the command followed by any options or arguments. For example, to display the current working directory, you can type `pwd`. The shell will then output the current directory.

Some common commands you may want to use in Bash include ls for listing the contents of a directory, cd for changing the current directory, and mkdir for creating a new directory.

## Basic syntax and structure of Bash scripts

Bash scripts are files that contain a series of Bash commands that are executed in sequence. The basic structure of a Bash script is as follows:

```
#!/bin/bash
# This is a comment
echo "Hello, world!"

```

The first line tells the shell to use Bash to interpret the script. The second line is a comment that provides a description of the script. Comments in Bash start with the # character and continue to the end of the line. The third line is a command that uses the echo command to print the message "Hello, world!" to the console.

## Using comments and whitespace

Comments and whitespace are important for making your Bash scripts easy to read and understand. Comments should be used to explain the purpose of the script, provide context for the commands, and make notes about the script. Whitespace should be used to separate commands and make the script easier to read.

## Running scripts from the command line

To run a Bash script from the command line, you need to make sure the file has executable permissions. You can do this by using the chmod command with the appropriate options. For example, to make a script named myscript.sh executable, you can type chmod +x myscript.sh. Once the file has executable permissions, you can run the script by typing ./myscript.sh in the terminal.

## Working with permissions and execution

In addition to setting executable permissions, you can also set permissions for reading, writing, and executing files in Bash. The chmod command allows you to modify file permissions for the owner, group, and others. The umask command can also be used to set default permissions for new files.

Congratulations, you have now learned the basics of syntax and commands in Bash! In the next lesson, we will cover variables and operators in Bash.