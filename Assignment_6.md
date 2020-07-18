## create a command that can only list hidden files and directories

### solution
  - code for command
```
#!/bin/bash
current=`pwd`
if [ $# -eq 0 ]
then
    echo "`ls -a $current  | grep '^\.'`"
else
    echo "`ls -a $1 | grep '^\.'`"
fi
```
