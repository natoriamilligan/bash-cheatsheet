## Bash Cheatsheet
### Basics
  - `#!/bin/bash` : every bash file must begin with this shebang tag that lets the syste, know which interpreter to use to run the script
  - `chmod +x bashname.sh` : you must make the file executable
  - `./` : use this before the file name to run the file

### Common Environment Variables
  - HOME
  - LOGNAME
  - SHELL
  - PATH

### Arguments
  - $1, $2, $3 represent arguments that can be passed in the terminal. (./arguments.sh hello world example --> each world will correlate with each number)

### Loops
  - `for arg in "$@"; do` end with `done` on same tab as "for"
