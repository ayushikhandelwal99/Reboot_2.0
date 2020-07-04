# run command without any output
### problem
  - open terminal and type any command
  - once you press enter your output of given command must not  print
  - you are not allowed to redirect output anywhere
  
### solution
  - (for this we can redirect the output to `any file` but as here it is prohibited so we will not do this)
  - for solving this problem we searched for the options of bash shell
  - we found an option `-D` it list double-quoted strings prefixed by $, but do not execute command in script
  - we run command `bash -D`
 
 <img src="https://i.ibb.co/ryRk74p/solution-6.png" alt="solution-6" border="0">
