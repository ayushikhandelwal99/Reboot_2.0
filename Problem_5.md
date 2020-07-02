# Play with files and directories
### problem
  - create 3 files named abc.txt ok fine g.txt under /tmp directory
  - create 4 directories a aa aaa aaaa under /tmp directory
  - give ls command to list the content of /tmp directory
  - make sure it will only list the content (file|directory)  having 2 char in their name
  
### solution
  - do cd to go to tmp directory in terminal
  - a file or directory with space in its name can be created by `firstname\ secondname\ so\ on`
  - `touch abc.txt ok\ fine g.txt` created 3 files
  - `mkdir a aa aaa aaaa` created 4 directories
  - `ls` command have so many options in which `-d` is used to show files/directories of specific character length. 
  - so for solving the question we used `ls -d ??` it means we need directory with two character length name only.
  
  <img src="https://i.ibb.co/C08JSZN/solution-5.png" alt="solution-5" border="0">
