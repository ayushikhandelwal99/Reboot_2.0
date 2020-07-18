# create a user with default settings

### problem
  - create a user name  delvex  and password of this user will be fedora
  - when user got created below listed things will come by default
  - history size will be 5000 
  - history file will be  /home/delvex/myhist.txt
  - default shell will be  /bin/sh 

### solution
  - `/etc/profile.d/` this directory contains mailbox files
  - run following
  ```
  cat <<N /etc/profile.d/delvex.sh
  if [ $USER == "delvex" ]
  then
          HISTSIZE=5000
          HISTFILE=/home/delvex/myhist.txt
          SHELL=/bin/sh
          export HISTSIZE HISTFILE SHELL
  fi
  N
  ```
  - Now run `adduser delvex`
  - This will create user delvex with above default settings

