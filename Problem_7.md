# Create a shell script
- create a shell script named /root/delvex.sh 
  - login to root
  - run `vim /root/delvex.sh`
- make sure it will run /bin/sh shell 
  - inside delvex.sh
  - write `#!/bin/sh`
  - press `Esc` and type `:wq`
  - run `chmod +x delvex.sh`
- a user will be running this script my using a command name opensource
  - run command `alias opensource='/root/delvex.sh'`
  - run `chmod +x opensource`
### inside script delvex.sh
- when a user  run like  "opensource  time" it must give current time only
  - for current time `date +%T`
- when it runs like "opensource user"  it will give list of interactive shell users only
  - for users `users`
- if runs like  "opensource windows"  then it must shutdown OS
  - for shutdown `shutdown now`
- if run opensource command without any parameter  then it must show out --
  - name of kernel 
    - `uname`
  - version of kernel 
    - `uname -r`
  - current date in the format of  /DD/MM/YY
    - `date +%d/%m/%y`
  - name of OS 
    - `hostnamectl | head -7 | tail -1`
  - last reboot time 
    - `who -b`
- when run like "opensource 100"  it must print "Hello Delvex" 100 times in interval of 1 sec
 *Note:    each output for last option must be in a separate line* 
 
 ## Script delvex.sh
``` 
 #!/bin/sh
re = '^[0-9]+$'
if [ "$#" -eq 0 ]
then
        echo "`uname`" 
        echo "`uname -r`"
        echo "`date +%d/%m/%y`"
        echo "`hostnamectl | head -7 | tail -1`"
        echo "`who -b`"
elif [ "$1" == 'user' ]
then
        echo "`users`"
elif [[ "$1" == $re ]]
then
        x=$1
        while [ $x !=0 ]
        do
                echo Hello Delvex 
                sleep 1
                (($x--))
        done
elif [ "$1" == 'windows' ]
then
        echo "`shutdown now`"
elif [ "$1" == "time" ]
then
        echo "`date +%T`"
else
        echo 'Give correct arguments'
fi
```
 
