![alt text](Linux.jpg)

# File Compression and Archiving with Tar in Linux

In this section we are going to learn file compression and archiving using Tar in Linux


## ```tar```

The **tar** command in Linux is a tool for managing and archiving files and directoriess.


## ```Archiving Files using tar```
Archiving file1.txt using **tar** command. To archive the file first we need to compress the file using **-c** switch and mention the file using **-f** and then provide the filename.
You need to use the switches together like **tar -cf (filename).tar (filename)**.
```
┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ tar -cf file1.tar file1.txt 
```
Checking the file using **file command**.
```
┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ file *
file1.tar: POSIX tar archive (GNU)
file1.txt: ASCII text
```

## ```Extracting Files using tar```
Let's learn how to extract files from their archived state. To extract files we are going to use **-x** switch in **tar**.
```
┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ tar -xf file1.tar 
```
You can use the **-v** switch for verbosity 
```
┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ tar -xvf file1.tar 
file1.txt
```


## ```gzip```

**gzip** command line utility is used to compress and decompress files in the Linux system.

## ```Compressing files in gzip format```
To compress files in gzip format we use **-z** switch in tar as shown below.
```
┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ tar -czf file1.tar.gz file1.txt 

┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ file file1.tar.gz 
file1.tar.gz: gzip compressed data, from Unix, original size modulo 2^32 10240
```

## ```Extracting files in gzip format```

To extract files or compressing files present in gzip format remember to use the **-z** switch which is for **gzip format** files.

```
┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ tar -xzf file1.tar.gz 

┌──(kali㉿kali)-[~/Desktop/Directory1]
└─$ ls
file1.tar.gz  file1.txt
```