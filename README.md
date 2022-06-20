# simple_shell


## Table of Contents
* [Description](#description)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)
* [Authors](#authors)
* [License](#license)

## Description
simple_shell is a command line interpreter, or shell, in the tradition of the first Unix shell written by Ken Thompson in 1971. This shell is intentionally minimalistic, yet includes the basic functionality of a traditional Unix-like command line user interface. 
Standard functions and system calls employed in simple_shell include:
   `access, execve, exit, fork, free, fstat, getline, malloc, perror, signal, stat, wait, write.`

## Requirements

simple_shell is designed to run in the `Ubuntu 20.04 LTS` linux environment and to be compiled using the GNU compiler collection v. `gcc 9.3.0` with flags`-Wall, -Werror, -Wextra, and -pedantic.`

## Installation

   - Clone this repository: `git clone "https://github.com/Gateg79/simple_shell.git"`
   - Change directories into the repository: `cd simple_shell`
   - Compile: `gcc -Wall -Werror -Wextra -pedantic *.c -o hsh`
   - Run the shell in interactive mode: `./hsh`
   - Or run the shell in non-interactive mode: example `echo "pwd" | ./hsh`

## Usage

The simple_shell is designed to execute commands in a similar manner to sh, however with more limited functionality. The development of this shell is ongoing. The below features will be checked as they become available (see man page for complete information on usage):

### Features
- [x] uses the PATH
- [x] implements builtins
- [x] handles command line arguments
- [x] custom strtok function
- [x] uses exit status
- [x] shell continues upon Crtl+C (**^C**)
- [x] handles comments (#)
- [x] handles **;**
- [x] custom getline type function
- [x] handles **&&** and **||**
- [x] aliases
- [x] variable replacement


### Builtins

- [x] exit
- [x] env
- [x] setenv
- [x] unsetenv
- [x] cd
- [x] help
- [x] history

### GCC command to compile:                                                                                                             
`                                                                                                                                       
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh                                                                                          
`                                                                                                                                       
                                                                                                                                        
This wil compile all the '.c' files and change the output's name to 'hsh'.                                                              
                                                                                                                                        
### Template to test output:                                                                                                            
=============                                                                                                                           
$ ./hsh                                                                                                                                 
                                                                                                                                        
($)                                                                                                                                     
                                                                                                                                        
hsh main.c shell.c                                                                                                                      
                                                                                                                                        
$ exit                                                                                                                                  
$                                                                                                                                       
                                                                                                                                        
                                                                                                                                        
sh``` in your shell.                                                                                                                    
                                                                                                                                        
The output after the program is executed should look something like this:                                                               
```                                                                                                                                     
$|                                                                                                                                      
```                                                                                                                                     
contents.                                                                                                                               
## Function Prototypes:                                                                                                                 
                                                                                                                                        
Brief description of functions contained in project:

**_strcmpdir** :  compares strings to find dir.                                                                                         
**find_command** :  finds command to execute in path routes.                                                                            
**charput** :  writes the character like putchar.                                                                                       
**place** :  similar to puts in C.                                                                                                      
**_strlen** :  string length.                                                                                                           
**str_concat** :  concatenate strings.                                                                                                  
**lookforslash** :  identify if first char is a '/'.                                                                                    
**compareExit** :  checks if user typed exit.                                                                                           
**compareEnv** :  checks if user typed env.                                                                                             
**execute_proc** :  receives command and args from getline to be executed.                                                              
**identify_string** :  returns pointer with folder address.                                                                             
**prompt** :  infinite loop with fork to keep prompt going.                                                                             
**controlC**: avoid program closing when pressing ctrl + c.                                                                             
**main**: initialize program.   

## Bugs
At this time, there are no known bugs.

## Authors
Agoha Anita | [GitHub](https://github.com/Anitachi)

Edikan Fred | [GitHub](https://github.com/Gateg79)

## License
simple_shell is open source and therefore free to download and use without permission.
