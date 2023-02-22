# polled-string-io<br>
An assembly program that processes user-input commands and receives and transmits characters to the terminal accordingly. The FRDM-KL05Z board from NXP is used.

![ProgramResults](https://github.com/Helena-Lynd/polled-string-io/blob/main/program-output.png?raw=true)

## Description<br>
When a microcontroller is given a user-input command, a certain flag is set which indicates that input has been received and needs to be processed. This program uses polling, a technique that continuously checks that status flag, to determine when to process commands. The program can process commands to save a user input string, determine the length of the string, have the string echoed to the terminal, and reset the string.
## Getting Started<br>
### Dependencies
- A method to compile the source files into an executable (e.g. Keil uVision5)
- KL05 board connected to a terminal (e.g. PuTTY)
### Installing
- Download the source files provided to your directory of choice
```
git clone git@github.com:Helena-Lynd/polled-string-io.git
```
- Compile the source files into an executable
  - If using an IDE, use the "Build" or "Rebuild" feature
### Executing
- Load the executable to your boards flash memory
  - If using an IDE, use the "Download" feature
- Run the program with a connected terminal window open
  - The board has a button that can be pressed to initiate the program
- Input one of the following commands (uppercase and lowercase commands are both accepted):
  - G : (Get String) Input a string to be saved.
  - I : (Initialize String) Resets the saved string to an empty string.
  - L : (Length of String) Prints the length of the saved string to the terminal.
  - P : (Put String) Prints the saved string to the terminal.
## Modifying
When using the Get String command (G), only up to 79 characters will be saved, even if more are input. This can be modified by updating the value of MAX_STRING in the EQUates section of the asm-src-code file.
## Authors<br>
Helena Lynd
