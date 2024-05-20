# Unix Shell Emulator

Developed for COSC 208: Introduction to Computer Systems in Fall 2023, this Unix Shell Emulator is a C-based application designed to replicate the functionality of a Unix shell. It offers essential shell commands, including the ability to manage background processes, providing educational insights into shell environments.

## Features
- **Command Parsing:** Breaks down user input into commands and arguments for execution.
- **Built-in Commands:** Supports `cd` for changing directories and `fg` for bringing background processes to the foreground.
- **Background Execution:** Enables commands to run in the background when followed by `&`, allowing for continuous shell use.
- **Signal Handling:** Handles `SIGCHLD` to clean up zombie processes and ignores `SIGINT` to prevent the shell from terminating with `Ctrl+C`.
- **Process Management:** Facilitates forking and executing commands, with appropriate management of foreground and background processes.

## Development
The development of this Unix Shell Emulator emphasized understanding process creation and management in Unix-like systems, user input parsing, and signal handling. Key challenges included managing background processes and intercepting signals to prevent shell termination.

## Acknowledgments
Special thanks to [Jon Cook](http://github.com/jon-cook1) for collaborating on this project.

## Usage
Compile the Unix Shell Emulator using a C compiler and run the resulting executable:

```sh
gcc -o shell_simulator shell_simulator.c
./shell_simulator

Once started, the shell presents a prompt (`shell> `) waiting for user input. Users can enter commands just like in a Unix shell. Special features include:

- To run a command in the background, append `&` at the end of the command.
- Use `cd [directory]` to change the current working directory.
- Use `fg` to continue the most recent background process in the foreground.
- Input `Ctrl+C` or type `exit` to quit the shell simulator.

