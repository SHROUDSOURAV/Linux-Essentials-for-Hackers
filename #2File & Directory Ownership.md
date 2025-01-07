![alt text](Linux.jpg)

# File and Directory Ownership using Linux

In this section we are going to learn about files and directories ownership using Linux.

## ```chown (Change File Ownership)```

**chown** command is used to modify ownership of a file or directory. But before ownership modification we need to check the current ownership of the file or directory using **ls -alh**.

The owner of **test.sh** is user **kali**.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  7 05:46  .
drwx------ 15 kali kali 4.0K Jan  7 05:40  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rw-rw-r--  1 kali kali   19 Jan  7 05:47  test.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

But let's say I want to change the file ownership to root. In that case we are going to use **chown** command as shown below.

Changing file ownership requires the user i.e kali to be in the **sudoers** file which we will talk about later. But as you can see after applying **chown** we have successfully given **root user** ownership of the file(test.sh).

```
┌──(kali㉿kali)-[~/Desktop]
└─$ sudo chown root test.sh 
[sudo] password for kali: 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  7 05:46  .
drwx------ 15 kali kali 4.0K Jan  7 05:40  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rw-rw-r--  1 root kali   19 Jan  7 05:47  test.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

## ```chgrp (Change Group Ownership)```

**chgrp** command is used to modify groups ownership of file/directory. Below is an example provided. As you can see the group ownership has changed. Same as **chown** the user needs to be in **sudoers** to change group ownerships.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ sudo chgrp root test.sh 
[sudo] password for kali: 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  7 05:46  .
drwx------ 15 kali kali 4.0K Jan  7 05:40  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rw-rw-r--  1 root root   19 Jan  7 05:47  test.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```