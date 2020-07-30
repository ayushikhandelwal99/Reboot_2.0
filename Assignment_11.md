## write a script which will work as useradd command

### solution
```
#!/bin/bash
# there are 10 changes we have to make to create a user

# 1 under /etc/passwd
# 2 under /etc/shadow
# 3 under /etc/group
# 4 under /etc/gshadow
# 5 under /home/
# 6 under /var/spool/mail/
# 7 data from /etc/skel/
# 8 security
# 9 access to PATH variable
# 10 kernal interaction

name=$1

id -u $name &> /dev/null  #to check if the user exist or not by checking its user id

if [ $? -ne 0 ]
then
        for i in {1000..60000}
        do
                id -u $i&>/dev/null & id -g $i&>/dev/null
                if [ $? -ne 0 ]
                then
                        break
                fi
        done
        uid=$i
        num_of_days=$((`date +%s` / 86400))
        echo "$name:x:$uid:$uid::/home/$name:/bin/bash">>/etc/passwd   #1
        echo "$name:!!:$num_of_days:0:99999:7:::">>/etc/shadow   #2
        echo "$name:x:$uid:">>/etc/group  #3
        echo "$name:!::">>/etc/gshadow  #4
        mkdir /home/$name       #5
        touch /var/spool/mail/$name    #6
        chown $name:$name /var/spool/mail/$name
        cp -a /etc/skel/. /home/$name/  #7
        chown $name:$name /home/$name/ -R
else
        echo "User '$name' already exists"
fi

```
