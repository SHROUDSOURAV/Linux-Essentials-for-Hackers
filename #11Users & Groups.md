![alt text](Linux.jpg)

# Users and Groups in Linux

In this section we are going learn about Users and Groups and their Permissions in Linux.

## ```visudo```

**visudo** command is opens the **/etc/sudoers** file and we can edit the file. To do that you need to be **root** or have **sudo** privileges. The sudoers file helps us customize which users and groups have **sudo** privileges to execute commands.
```
# User privilege specification
root    ALL=(ALL:ALL) ALL

# Allow members of group sudo to execute any command
%sudo   ALL=(ALL:ALL) ALL

# See sudoers(5) for more information on "@include" directives:
```

## ```useradd```

**useradd** command is used to add users in Linux. I am going to add user without using **root** so I need to execute the commands using **sudo**.

## ```Adding New User and giving Sudo Privileges```

- Step 1 -> adding new user and giving home directory using **-m** switch in the **useradd** command.
```
┌──(kali㉿kali)-[~]
└─$ sudo useradd Testuser
[sudo] password for kali: 
```

To confirm whether we have successfully added our new user we can use the below command to confirm.
```
┌──(kali㉿kali)-[~]
└─$ cat /etc/passwd | grep "Testuser"
Testuser:x:1001:1001::/home/Testuser:/bin/sh
```

- Step 2 -> Giving password to the new user by executing the below command. If giving new password doesn't work give the password of the user you use by default and change it later.
```
┌──(kali㉿kali)-[~]
└─$ sudo passwd Testuser
New password: 
Retype new password: 
passwd: password updated successfully
```

- Step 3 -> Now we need to provide the new user with **sudo privileges** by executing the below command. **-a** for adding user and **-G sudo** for adding the user to the **sudoers group**.
```
┌──(kali㉿kali)-[~]
└─$ sudo usermod -a -G sudo Testuser
```

- Step 4 -> Let's verify whether we can execute **sudo su** in as the new user to switch to **root** user. 
```
┌──(kali㉿kali)-[~]
└─$ su Testuser
Password: 
$ sudo su
[sudo] password for Testuser: 
┌──(root㉿kali)-[/home/kali]
└─# 
```
We successfully added a new user and gave it sudo privileges.

## ```userdel```

**userdel** command is used to delete a user in Linux.

## ```Deleting User```

Let's delete the new user we added previously.
```
┌──(kali㉿kali)-[~]
└─$ sudo userdel Testuser
[sudo] password for kali: 
```

Now after executing the above command it might show that the user you are trying to delete is being used by some other processes, in that case reboot the session and execute the command again.

To confirm whether our deletion worked successfully let's execute the below command.
```
┌──(kali㉿kali)-[~]
└─$ cat /etc/passwd | grep "Testuser"

```

So the above command doesn't show us any userID or anything since the **Testuser** doesn't exist so we successfully deleted the user.


## ```Checking the groups user is associated with```

All the groups are present in **/etc/group**. So to check the groups the current user is associated with we can use 2 methods.

- Method 1
```
┌──(kali㉿kali)-[~]
└─$ groups
kali adm dialout cdrom floppy sudo audio dip video plugdev users netdev bluetooth scanner wireshark kaboxer
```

- Method 2
```
┌──(kali㉿kali)-[~]
└─$ cat /etc/group | grep "kali"
adm:x:4:kali
dialout:x:20:kali
cdrom:x:24:kali
floppy:x:25:kali
sudo:x:27:kali
audio:x:29:pulse,kali
dip:x:30:kali
video:x:44:kali
plugdev:x:46:kali
users:x:100:kali
netdev:x:101:kali
bluetooth:x:106:kali
scanner:x:113:saned,kali
kali-trusted:x:119:
wireshark:x:136:kali
kali:x:1000:
kaboxer:x:137:kali
```