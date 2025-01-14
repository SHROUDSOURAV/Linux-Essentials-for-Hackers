![alt text](Linux.jpg)

# Disk Usage in Linux

In this section we are going to learn about disk usage of the Linux system.

## ```du```

**du** command utility is used to estimate disk usage in Linux system. Let's run a simple **du** command and see what happens.

Ok, so **du** is showing a lot of output. It's basically showing the sizes of all files recursively in the current directory.
```
┌──(kali㉿kali)-[~]
└─$ du
4       ./Documents
8       ./.config/powershell
8       ./.config/gtk-3.0
8       ./.config/gedit
4       ./.config/qt5ct/qss
4       ./.config/qt5ct/colors
16      ./.config/qt5ct
8       ./.config/nautilus
8       ./.config/Thunar
4       ./.config/qt6ct/qss
4       ./.config/qt6ct/colors
16      ./.config/qt6ct
4       ./.config/enchant
8       ./.config/pulse
24      ./.config/xfce4/desktop
4       ./.config/xfce4/xfwm4
8       ./.config/xfce4/panel/launcher-5
16      ./.config/xfce4/panel/launcher-7
8       ./.config/xfce4/panel/launcher-6
40      ./.config/xfce4/panel
80      ./.config/xfce4/xfconf/xfce-perchannel-xml
84      ./.config/xfce4/xfconf
160     ./.config/xfce4
8       ./.config/cherrytree
8       ./.config/dconf
12      ./.config/qterminal.org
12      ./.config/ristretto
300     ./.config
8       ./.java/.userPrefs/burp
12      ./.java/.userPrefs
16      ./.java
4       ./Public
4       ./Templates
4       ./Videos
108     ./Desktop/Java Apna College
176     ./Desktop/Assembly Codes
300     ./Desktop
8       ./.local/state/wireplumber
16      ./.local/state
8       ./.local/share/powershell/PSReadLine
4       ./.local/share/powershell/Modules
16      ./.local/share/powershell
12      ./.local/share/keyrings
8       ./.local/share/gedit
8       ./.local/share/nano
8       ./.local/share/nautilus/scripts
12      ./.local/share/nautilus
4       ./.local/share/icc
44      ./.local/share/gvfs-metadata
4       ./.local/share/ristretto
120     ./.local/share
140     ./.local
456     ./Pictures
4       ./Music
4       ./Downloads
4       ./.gnupg/private-keys-v1.d
8       ./.gnupg
8       ./.cache/powershell
1392    ./.cache/gstreamer-1.0
36      ./.cache/vmware/drag_and_drop/YSD9hX
20      ./.cache/vmware/drag_and_drop/fmyyYy
148     ./.cache/vmware/drag_and_drop/ituzNH
16      ./.cache/vmware/drag_and_drop/GsDEp1
224     ./.cache/vmware/drag_and_drop
228     ./.cache/vmware
8       ./.cache/mesa_shader_cache/f1
8       ./.cache/mesa_shader_cache/b9
8       ./.cache/mesa_shader_cache/a8
1312    ./.cache/mesa_shader_cache
16      ./.cache/sessions/thumbs-kali:0
24      ./.cache/sessions
24      ./.cache/xfce4/notifyd
28      ./.cache/xfce4
420     ./.cache/thumbnails/normal
28      ./.cache/thumbnails/large
452     ./.cache/thumbnails
4       ./.cache/obexd
3504    ./.cache
4872    .
```

Let's optimize the output and use some switches in the **du** command to get better human readable results. K = Kilobytes.

You can see the list of directories and each of their individual sizes have been provided.
```
┌──(kali㉿kali)-[~]
└─$ du -sh *
300K    Desktop
4.0K    Documents
4.0K    Downloads
4.0K    Music
456K    Pictures
4.0K    Public
4.0K    Templates
4.0K    Videos
```

Let's say you want to only see Kilobytes files so you can filter the search using **grep** command to pipe the output from the **du** output process.
```
┌──(kali㉿kali)-[~]
└─$ du -sh * | grep "K"
300K    Desktop
4.0K    Documents
4.0K    Downloads
4.0K    Music
456K    Pictures
4.0K    Public
4.0K    Templates
4.0K    Videos
```

If you want to check the total size of all the files and directories in the current working directory use the **-c** switch of the **du** command.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ du -shc *
176K    Assembly Codes
108K    Java Apna College
12K     util.asm
296K    total
```

## ```df```

**df** command utility gives us information or provides details of the disk usage in the Linux system. **df -h** shows us the size in human readable format.
```
┌──(kali㉿kali)-[~]
└─$ df -h
Filesystem      Size  Used Avail Use% Mounted on
udev            2.9G     0  2.9G   0% /dev
tmpfs           599M  1.3M  598M   1% /run
/dev/sda1        79G   15G   60G  20% /
tmpfs           3.0G     0  3.0G   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-journald.service
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-udev-load-credentials.service
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-sysctl.service
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-tmpfiles-setup-dev-early.service
tmpfs           3.0G  8.0K  3.0G   1% /tmp
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-tmpfiles-setup-dev.service
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-tmpfiles-setup.service
tmpfs           1.0M     0  1.0M   0% /run/credentials/getty@tty1.service
tmpfs           599M  128K  599M   1% /run/user/1000
```

Let's say I only want to see the disk usage details of the storage devices in the Linux system.**Piping** the output of **df -h** process using **grep** to filter the output and get better results.
```
┌──(kali㉿kali)-[~]
└─$ df -h | grep "sd"
/dev/sda1        79G   15G   60G  20% /
```