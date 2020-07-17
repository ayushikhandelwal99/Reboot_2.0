## Do following:
- write a script which performs something
	- run it
	- if successfully runned then convert the script in binary
	- put that script under /usr/bin/
 *Note: when doing cat command the outcome should be like that no one can read it*
 
 
- write a script and run it
	- `vim random.sh`
	-
		#!/bin/bash
		read -p "How many random numbers do you want to generate? "  max
		for((start=1; start <= $max; start++ ))
		do
        	echo -e $RANDOM
		done
- if successful then convert it in binary
	- `shc -f random.sh`		
- it will create 3 files named
	- random.sh (original one)
	- random.sh.x (binary format)
	- random.sh.x.c (C source code, it is compiled to create random.sh.x)
- put that under /usr/bin/
	- `mv random.sh.x  /usr/bin/random`
		
- Now when you run `which random` it will give path of command as `/usr/bin/random`
- then if you open that file, everything is `blah` for you now. {you will get binary format}
		
	
