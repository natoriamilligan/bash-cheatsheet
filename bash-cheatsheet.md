## Bash Cheatsheet
### Basics
  - `#!/bin/bash` : every bash file must begin with this shebang tag that lets the syste, know which interpreter to use to run the script
  - `chmod +x bashname.sh` : you must make the file executable
  - `./` : use this before the file name to run the file
  - `@` : means all elements
  - `#` : tells systems to count
  - `$#` : represents the number of arguments you passed into terminal when running the script

### Variables
  - `result=$(add $num1 $num2)` : this is a command syntax, the first element is a function and the following elements are the arguments to put in that function.         Result stores what is return fromthe function
  #### Common Environment Variables
  - HOME
  - LOGNAME
  - SHELL
  - PATH

### Arguments
  - $1, $2, $3 represent arguments that can be passed in the terminal. (./arguments.sh hello world example --> each world will correlate with each number)

### Conditional Statements
  `return 1` : returning a non-zero number indicates an error
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
  #### Case Statements
  - ```
    case $operation in
      plus)
        result=$((num1 + num2))
        echo "$num1 + $num2 = $result"
        ;;
    esac```

### Loops
  - `for arg in "$@"; do` end with `done` on same tab as "for"
  - use `{1..5}` : to loop through numbers 1-5
  - `while [ $count -g 0 ]; do` : very similar to for loops
  - `sleep 1` : added to a for loop block pauses for 1 second
  - `until loop` : similar to while loops, but keeps executing until the condition is true. (opposite of while loops)

### Arrays
  - `NUMBERS=()` : initializes an array called numbers
  - `NUMBERS+=(1)` : adds an element "1" to the numbers array
  - `a=(3 5 8 10 6)` : array elements are separated by spaces

### String Operations
  - `${#string}` : count the length of the string
  - `$(expr index "$string" "$char")` : find the index of a character in a string
  - `${string:start:length}` : print the string starting from "start" and going however the "length" you want
  - `${string/pattern/replacement}` : replace the first occurance of pattern with replacement
  - `${string//pattern/replacement}` : replace all occurances of pattern with replacement
  - `${string/#pattern/replacement}` : replace pattern with replacement if pattern is at the beginning of the string
  - `${string/%pattern/replacement}` : replace pattern with replacement if pattern is at the end of the string

### Arithmetic
  - `$((x - 1))` : two paraentheses to do an equation

### Functions
  - to run a function you just need the function name (no parentheses)
  - functions return either an echoed result or a variable that was declared in the function
  - `local LACAL_VAR="I'm a local variable"` : Local variables can be declared that stay inside the function and are not global
  
    #### Parameters
    - parameters are still used using the arguments -->> $1 $2 $3 etc. **However you specify the arguments in the bash file not the terminal**
