![alt text](Linux.jpg)

# File Management and Manipulation using Linux

In this section we are going to learn file management and manipulation using various Linux commands.

## pwd

**pwd** command is used to check the location of the current directory in linux. Here we can see are in home directory and the user in kali.

```
┌──(kali㉿kali)-[~]
└─$ pwd
/home/kali
```

This shows that we are currently in the **home** directory of user kali.

## ls

ls command to list files and directories of the current path in linux.

```
┌──(kali㉿kali)-[~]
└─$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
```

We can use the ls -l command to list the files and directories in a list format. ls -l command gives us crucial information about the files and directories permissions and who are its owners.

```
┌──(kali㉿kali)-[~]
└─$ ls -l
total 32
drwxr-xr-x 3 kali kali 4096 Dec 30 12:32 Desktop
drwxr-xr-x 2 kali kali 4096 Dec  3 13:57 Documents
drwxr-xr-x 2 kali kali 4096 Dec  3 13:57 Downloads
drwxr-xr-x 2 kali kali 4096 Dec  3 13:57 Music
drwxr-xr-x 2 kali kali 4096 Dec 30 11:41 Pictures
drwxr-xr-x 2 kali kali 4096 Dec  3 13:57 Public
drwxr-xr-x 2 kali kali 4096 Dec  3 13:57 Templates
drwxr-xr-x 2 kali kali 4096 Dec  3 13:57 Videos
```

To list all the files and directories both hidden and not hidden we use the ls -al command. The -a switch is used to list basically and the files and directories hidden or not hidden alike. The files starting with dot(.) are basically hidden so -a switch helps us to list those files. The -h list the files in human readable format i.e. in kilobytes(KB).

```
┌──(kali㉿kali)-[~]
└─$ ls -alh
total 176K
drwx------ 15 kali kali 4.0K Jan  6 12:35 .
drwxr-xr-x  3 root root 4.0K Aug 18 15:57 ..
-rw-------  1 kali kali  22K Dec 30 12:34 .bash_history
-rw-r--r--  1 kali kali  220 Aug 18 15:57 .bash_logout
-rw-r--r--  1 kali kali 5.5K Aug 18 15:57 .bashrc
-rw-r--r--  1 kali kali 3.5K Aug 18 15:57 .bashrc.original
drwxrwxr-x  9 kali kali 4.0K Dec 14 12:19 .cache
drwxr-xr-x 16 kali kali 4.0K Dec 29 10:40 .config
drwxr-xr-x  3 kali kali 4.0K Dec 30 12:32 Desktop
-rw-r--r--  1 kali kali   35 Dec  3 13:57 .dmrc
drwxr-xr-x  2 kali kali 4.0K Dec  3 13:57 Documents
drwxr-xr-x  2 kali kali 4.0K Dec  3 13:57 Downloads
-rw-r--r--  1 kali kali  12K Aug 18 15:57 .face
lrwxrwxrwx  1 kali kali    5 Aug 18 15:57 .face.icon -> .face
drwx------  3 kali kali 4.0K Dec  3 13:57 .gnupg
-rw-------  1 kali kali    0 Dec  3 13:57 .ICEauthority
drwxr-xr-x  3 kali kali 4.0K Aug 18 15:57 .java
drwxr-xr-x  4 kali kali 4.0K Dec  3 13:57 .local
drwxr-xr-x  2 kali kali 4.0K Dec  3 13:57 Music
drwxr-xr-x  2 kali kali 4.0K Dec 30 11:41 Pictures
-rw-r--r--  1 kali kali  807 Aug 18 15:57 .profile
drwxr-xr-x  2 kali kali 4.0K Dec  3 13:57 Public
-rw-------  1 kali kali  276 Dec 14 03:40 .python_history
-rw-r--r--  1 kali kali    0 Dec  3 13:58 .sudo_as_admin_successful
drwxr-xr-x  2 kali kali 4.0K Dec  3 13:57 Templates
drwxr-xr-x  2 kali kali 4.0K Dec  3 13:57 Videos
-rw-------  1 kali kali  11K Dec 13 14:46 .viminfo
-rw-rw-r--  1 kali kali  215 Dec 14 13:17 .wget-hsts
-rw-------  1 kali kali   49 Jan  6 12:35 .Xauthority
-rw-------  1 kali kali 4.0K Jan  6 12:35 .xsession-errors
-rw-------  1 kali kali 4.4K Dec 30 12:34 .xsession-errors.old
-rw-------  1 kali kali 1.1K Dec  6 12:18 .zsh_history
-rw-r--r--  1 kali kali  11K Aug 18 15:57 .zshrc
```

To list the files of a directory and its subdirectories we use ls -lR to recursively list the files.  We can see that the files and directories in Desktop are displayed and also the files under Assembly Codes directory under Desktop are also displayed.

```
┌──(kali㉿kali)-[~]
└─$ ls -lR Desktop/
Desktop/:
total 16
drwxrwxr-x 2 kali kali  4096 Dec 30 06:59 'Assembly Codes'
-rw-rw-r-- 1 kali kali     0 Dec 30 12:32  file.txt
-rw-rw-r-- 1 kali kali 10837 Dec 18 14:46  util.asm

'Desktop/Assembly Codes':
total 172
-rwxrwxr-x 1 kali kali  9840 Dec 14 12:14 1
-rw-rw-r-- 1 kali kali  2224 Dec 14 12:14 1.o
-rw-rw-r-- 1 kali kali    20 Dec 13 12:44 key
-rw-rw-r-- 1 kali kali     0 Dec 13 12:44 key.txt
-rwxrwxr-x 1 kali kali  9296 Dec 14 06:59 License
-rw-rw-r-- 1 kali kali  1499 Dec 14 03:39 License.asm
-rw-rw-r-- 1 kali kali  1520 Dec 14 06:59 License.o
-rwxrwxr-x 1 kali kali  8840 Dec  3 14:03 prog1
-rw-rw-r-- 1 kali kali   313 Dec  3 14:03 prog1.asm
-rw-rw-r-- 1 kali kali   848 Dec  3 14:03 prog1.o
-rwxrwxr-x 1 kali kali  9064 Dec  6 14:08 prog2
-rw-rw-r-- 1 kali kali  1204 Dec  6 14:07 prog2.asm
-rw-rw-r-- 1 kali kali  1184 Dec  6 14:07 prog2.o
-rwxrwxr-x 1 kali kali  4864 Dec  6 14:04 prog3
-rw-rw-r-- 1 kali kali   484 Dec 13 03:22 prog3.asm
-rw-rw-r-- 1 kali kali   944 Dec  6 14:04 prog3.o
-rwxrwxr-x 1 kali kali  4728 Dec 13 04:15 prog4
-rw-rw-r-- 1 kali kali   854 Dec 13 04:13 prog4.asm
-rw-rw-r-- 1 kali kali   656 Dec 13 04:13 prog4.o
-rwxrwxr-x 1 kali kali  9288 Dec 14 03:39 prog5
-rw-rw-r-- 1 kali kali  1499 Dec 14 11:14 prog5.asm
-rw-rw-r-- 1 kali kali  1520 Dec 14 03:39 prog5.o
-rwxrwxr-x 1 kali kali  9984 Dec 14 14:37 prog6
-rw-rw-r-- 1 kali kali  1826 Dec 14 14:37 prog6.asm
-rw-rw-r-- 1 kali kali  2464 Dec 14 14:37 prog6.o
-rwxrwxr-x 1 kali kali 10584 Dec 15 12:14 prog7
-rw-rw-r-- 1 kali kali  2165 Dec 15 12:14 prog7.asm
-rw-rw-r-- 1 kali kali  3584 Dec 15 12:14 prog7.o
```

## cd

The cd command is used to navigate back and forth the directories of linux . To go to the previous directory we use the cd ..

```
┌──(kali㉿kali)-[~]
└─$ pwd
/home/kali

┌──(kali㉿kali)-[~]
└─$ cd ..

┌──(kali㉿kali)-[/home]
└─$ pwd
/home
```

To move to the next directory we can do cd (directory_name). Shortcut to go to home directory --->  cd ~

```
┌──(kali㉿kali)-[/home]
└─$ pwd
/home

┌──(kali㉿kali)-[/home]
└─$ cd kali/Desktop/

┌──(kali㉿kali)-[~/Desktop]
└─$ pwd
/home/kali/Desktop
```

## touch

The touch command is used to create files in linux easily. 

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch file.txt

┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt   util.asm
```

## echo

**echo** command is used to print a line of text.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ echo "kali linux"
kali linux
```

we can also use **>** symbol along with **echo** to redirect data or content into the file.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ echo "hello world" > file.txt 
```

## cat

**cat** command is used to display the data/contents of the file.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cat file.txt 
hello world
```

we can also use the cat command to redirect output.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cat file.txt > file2.txt

┌──(kali㉿kali)-[~/Desktop]
└─$ cat file2.txt 
hello world
```

## rm 

**rm** command is used to deleted a file.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file2.txt   file.txt   util.asm

┌──(kali㉿kali)-[~/Desktop]
└─$ rm file2.txt 

┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt   util.asm
```

To delete a directory or folder we need to use the **-R** switch of the **rm** command to recursively delete the specific directory.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt  'Test Directory'   util.asm

┌──(kali㉿kali)-[~/Desktop]
└─$ rm -R Test\ Directory

┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt   util.asm
```

## mkdir 

**mkdir** command is used to create a directory.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir Test

┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt   Test   util.asm
```

## cp

**cp** command is used to copy a file or directory. The syntax of using this command is to first specify the file you want to copy and then the destination path using **/** but since I am copying the file to a directory of the current path I do not need to specify it again.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt   Test   util.asm

┌──(kali㉿kali)-[~/Desktop]
└─$ cp file.txt Test/

┌──(kali㉿kali)-[~/Desktop]
└─$ ls -alh Test/
total 12K
drwxrwxr-x 2 kali kali 4.0K Jan  6 13:54 .
drwxr-xr-x 4 kali kali 4.0K Jan  6 13:50 ..
-rw-rw-r-- 1 kali kali   12 Jan  6 13:54 file.txt
```

## mv

**mv** command is used to move a file or directory. We can also use **mv** to rename a file or directory.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mv file.txt Test/

┌──(kali㉿kali)-[~/Desktop]
└─$ ls Test/
file.txt
```

To rename a file using **mv** command is shown below.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file.txt   Test   util.asm

┌──(kali㉿kali)-[~/Desktop]
└─$ mv file.txt file2.txt

┌──(kali㉿kali)-[~/Desktop]
└─$ ls
'Assembly Codes'   file2.txt   Test   util.asm
```