##  Without using factor command write a script which will run like factor.

### solution-->
```
#!/bin/bash
#this script works as factor command
n=$1
declare -a list=()
while [ $(( $n%2)) -eq 0 ]
do
        list+="2 "
        ((n=n/2))
done
sqrt=`bc <<< "scale=0; sqrt($n)"`
for((i=3; i<=$sqrt; $((i=i+2))))
do
        while [ $(($n%$i)) -eq 0 ]
        do
                list+="$i "
                ((n=n/$i))
        done
done
if [ $n -gt 2 ]
then
        list+="$n "
fi

echo "$1: ${list[@]}"

```
