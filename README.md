# Reboot_2.0
### Important links

1 .[PowerShell Constrained languages](https://devblogs.microsoft.com/powershell/powershell-constrained-language-mode/)

2 .[How to freeze your screen or lock your linux system from command line](https://www.networkworld.com/article/3438818/how-to-freeze-and-lock-your-linux-system-and-why-you-would-want-to.html)

3 .[System and Administrative commands](https://tldp.org/LDP/abs/html/system.html)

4 .[Behind the scene: how commands execute](https://medium.com/@SergioPietri/behind-the-scenes-what-happens-when-you-execute-a-command-in-the-shell-9fef53832f6a)

### How to write in a directory
Directory is a kind of file that is used to map different (files) 
we can not write something as a text in a directory as it is designed to store other files
but we can add some extra file or directory information just like ACL permissions
the above task can be done using setfattr command which is to declare new attribute or information within meta data of file
     
 1. Run ```mkdir hey``` 
 2. Run ```setfattr -n user.text -v "Hey this is a way to write in a directory" hey```
 3. For output run ```getfattr -n user.text Greetings```
   ```
  file: Greetings
  user.text="Hey this is a way to write in a directory"
  ```
  
 ## files
- /etc/passwd
     - User account information.

- /etc/shadow
     - Secure user account information.

- /etc/group
     - Group account information.

- /etc/default/useradd
     - Default values for account creation.

- /etc/skel/
     - Directory containing default files.

- /etc/login.defs
     - Shadow password suite configuration.

### Solution 1
   
### Solution 2
<img src="https://github.com/ayushikhandelwal99/Reboot_2.0/blob/master/screenshots_of_solutions/Solution_2.png?raw=true">

