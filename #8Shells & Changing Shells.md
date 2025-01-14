![alt text](Linux.jpg)

# Shells and Changing Shells in Linux

In this section we are going to learn about shells and how to change shells in Linux.

## ```Shell```

A **shell** is basically a program in the terminal which helps the user to interpret and execute commands. In Linux there are many shells like **sh**, **bash**, **zsh** etc.

Command to check the shell you are using. Using the **echo** displays that I am using the **bash** shell.
```
┌──(kali㉿kali)-[~]
└─$ echo $SHELL
/usr/bin/bash
```

Let's check the path of the other shells in the Linux system using the below command.
```
┌──(kali㉿kali)-[~]
└─$ cat /etc/shells
# /etc/shells: valid login shells
/bin/sh
/usr/bin/sh
/bin/bash
/usr/bin/bash
/bin/rbash
/usr/bin/rbash
/bin/dash
/usr/bin/dash
/usr/bin/tmux
/bin/zsh
/usr/bin/zsh
/usr/bin/pwsh
/opt/microsoft/powershell/7/pwsh
/usr/bin/screen
```

Let's switch shells and try a few commands and see if that works. I will be switching to **sh** shell.
```
┌──(kali㉿kali)-[~]
└─$ sh
$ id
uid=1000(kali) gid=1000(kali) groups=1000(kali),4(adm),20(dialout),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),100(users),101(netdev),106(bluetooth),113(scanner),136(wireshark),137(kaboxer)
$ whoami
kali
$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
$ exit
```

## ```chsh```

**chsh** command used to change shell in the Linux. You also need to specify the path of the particular shell you are going to use by executing the **cat /etc/shells** command. After changing the shell remember to login again and check the current shell using **echo $SHELL** command.
```
┌──(kali㉿kali)-[~]
└─$ chsh
Password: 
Changing the login shell for kali
Enter the new value, or press ENTER for the default
        Login Shell [/usr/bin/bash]: /usr/bin/zsh
```

I am changing to **zsh** shell you can try other shells too but make sure to set the path accordingly. After executing the above steps login again and check.

After logging in again you can see my shell has changed.
```
┌──(kali㉿kali)-[~]
└─$ echo $SHELL
/usr/bin/zsh
```
