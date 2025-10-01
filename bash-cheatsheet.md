## Bash Cheatsheet
### Basics
  - `#!/bin/bash` : every bash file must begin with this shebang tag that lets the syste, know which interpreter to use to run the script
  - `chmod +x bashname.sh` : you must make the file executable
  - `./` : use this before the file name to run the file
  - `@` : means all elements
  - `#` : tells systems to count
  - `$#` : represents the number of arguments you passed into terminal when running the script

### Common Environment Variables
  - HOME
  - LOGNAME
  - SHELL
  - PATH

### Arguments
  - $1, $2, $3 represent arguments that can be passed in the terminal. (./arguments.sh hello world example --> each world will correlate with each number)

### Conditional Statements
  #### Comparison Operators
    - lt : less than
    - gt : greater than
    - eq : equal to
    - le : less than or equal
    - ne : not equal to
  #### String Comparisons and Logical Operators
    - **When comparing using -z or != or = make sure to use double brackets [[]] in the if statements** (not needed when using logical operators like || and &&
    - != : used for strings 
    - `-z` : ask if a string is empty

### Loops
  - `for arg in "$@"; do` end with `done` on same tab as "for"

### Arrays
  - `NUMBERS=()` : initializes an array called numbers
  - `NUMBERS+=(1)` : adds an element "1" to the numbers array

### String Operations
  - `${#string}` : count the length of the string
  - `$(expr index "$string" "$char")` : find the index of a character in a string
  - `${string:start:length}` : print the string starting from "start" and going however the "length" you want
  - `${string/pattern/replacement}` : replace the first occurance of pattern with replacement
  - `${string//pattern/replacement}` : replace all occurances of pattern with replacement
  - `${string/#pattern/replacement}` : replace pattern with replacement if pattern is at the beginning of the string
  - `${string/%pattern/replacement}` : replace pattern with replacement if pattern is at the end of the string
