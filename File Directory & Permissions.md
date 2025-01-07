![alt text](Linux.jpg)

# File Directory and Permissions using Linux

In this section we are going to learn about linux files and directory permissions in detail.

To list the permissions of all files and directories in the current path you are in use **ls -al** command which is going to show the file ownership, date of modification, file size, and file permissions(**read**, **write**, **executable**).

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls -al
total 24
drwxr-xr-x  3 kali kali  4096 Jan  6 14:07  .
drwx------ 15 kali kali  4096 Jan  6 22:09  ..
drwxrwxr-x  2 kali kali  4096 Dec 30 06:59 'Assembly Codes'
-rw-rw-r--  1 kali kali 10837 Dec 18 14:46  util.asm
```

## File Size

The **4096** or **10837** defines the file size in **bytes**.

## Date of Modification

You can easily see the dates mentioned along the file size written in Jan 6 or in any other dates. These dates state the timing of the file/directory modification of any sort.

## File Permissions 
- Directory = d
- Read  = r
- Write = w
- Executable = x

As you can see there are multiple combinations of rwx in **util.asm** file. Let me explain what that means...
```
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

-rw
- file owner permissions

-rw
- group owner permissions

-r
- other permissions -> this means that if I were to be logged as a user other than ower user(**kali**) or group owner (**kali**) I will only have **read permissions**.

## Change Mode of File Permissions

We can change the mode of file permissions using **chmod** command in linux.

There are 2 ways to implement **chmod** command to mofify file permissions.

- Symbolic mode Format
- Octal Mode Format

### **```SYMBOLIC MODE FORMAT```**

Let's consider there is a file named prog1.sh having permissions as stated below. 

```
┌──(kali㉿kali)-[~/Desktop]
└─$ echo "echo 'Hello world'" > prog1.sh

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:03  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rw-rw-r--  1 kali kali   12 Jan  6 23:06  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

Let's try to execute the file and see what happens. This means that user **kali** dosen't have executable permissions for the file.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ ./prog1.sh
bash: ./prog1.sh: Permission denied
```

Now let's give (read, write, executable) permissions to **kali** user using ***Symbolic Mode Format*** and check file permissions using **ls -alh**.

u = user 

u = rwx gives read, write and executable permissions to file owner.

You can also modify permissions for groups and others. User to Group(g) or User to Other(o)

Below are mentioned examples of modifying group and other permissions respectively.

**go** specifies (groups and others) together. We set their permissions to read only as shown below
```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod go=r prog1.sh 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:27  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rwxr--r--  1 kali kali   19 Jan  6 23:27  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

Now, we are going to add read, write, and exectuable permissions to **kali** user.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod u=rwx prog1.sh 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:03  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rwxrw-r--  1 kali kali   12 Jan  6 23:06  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

 Let's try to execute **prog1.sh** again...

We can see **prog1.sh** successfully executed and printed **Hello World** :)

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ./prog1.sh 
Hello world
```

## Removing File Permissions

We have learnt about how to add permissions to user,groups and others but we also need to learn how to remove certain permissions, which we are going to learn in this section.


Removing permissions is almost the same as adding them except we use (**-**) symbol to remove the permissions whereas (**=**) to add them. Below is an example to remove permissions for groups and others.

**We are removing the write(w) and executable(x) permissions for groups and others(go).**
```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod go-xw prog1.sh 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:27  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rwxr--r--  1 kali kali   19 Jan  6 23:27  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

**To add write(w) and executable(x) permissions back to groups and others(go)**

```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod go+wx prog1.sh 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:27  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rwxrwxrwx  1 kali kali   19 Jan  6 23:27  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

### **```OCTAL MODE FORMAT```**

In symbolic mode format we used user = u, groups = g, others = o but in ***Octal Mode Format*** rwx i.e read, write, and executable are represented as :-

**read(r) = 4**

**write(w) = 2**

**executable(x) = 1**

Now if I were to give executable permissions to user I will use **chmod 100 prog1.sh**. You might have noticed **00** and wonder what does that represent??? **The first 0 defines permissions for the groups** and **the second 0 defines permissions for others**. 

Giving **0** value to either user, groups or others means they don't have either read(r), write(w), or executable(x) permissions.

Check the commands to understand the application of the above scenario.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod 100 prog1.sh 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:27  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
---x------  1 kali kali   19 Jan  6 23:27  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```

Using the Octal Mode Format if we want to add or remove permissions we need to change our 4,2,1 values for users, groups, and others. Now let's say we want to give (rwx) permissions to user and (r) permissions to groups and others.

**Why 744???**

7 = 4(r) + 2(w) + 1(x) for users

4 = read permissions for groups and others.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod 744 prog1.sh 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh
total 28K
drwxr-xr-x  3 kali kali 4.0K Jan  6 23:27  .
drwx------ 15 kali kali 4.0K Jan  6 22:09  ..
drwxrwxr-x  2 kali kali 4.0K Dec 30 06:59 'Assembly Codes'
-rwxr--r--  1 kali kali   19 Jan  6 23:27  prog1.sh
-rw-rw-r--  1 kali kali  11K Dec 18 14:46  util.asm
```