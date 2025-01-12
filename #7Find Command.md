![alt text](Linux.jpg)

# Find Command usage in Linux

In this section we are going to learn how to use the find command utility in Linux.


## ```find```

**find** command is used to find files or directories in the Linux system. We need to mention the path of the file/directory we are trying to find and the type (file/directory). In **find** command **./** means current path and **/** means all the files and directories in the Linux system.

Important points to remember while searching for a file using **find** command to get optimized results.
-   path/location 
-   type (file/directory)
-   file/directory name

To list the entire file system of Linux you can use **find /** command. You need **sudo** priviledges for it. Below we are just going to list the files of the current path using **find ./** command. Such searches are inefficient as you can very well understand due to the immense number of output.
```
┌──(kali㉿kali)-[~]
└─$ find ./
./
./Documents
./.face.icon
./.config
./.config/powershell
./.config/powershell/Microsoft.PowerShell_profile.ps1
./.config/gtk-3.0
./.config/gtk-3.0/bookmarks
./.config/gedit
./.config/gedit/accels
./.config/qt5ct
./.config/qt5ct/qt5ct.conf
./.config/qt5ct/qss
./.config/qt5ct/colors
./.config/nautilus
./.config/nautilus/scripts-accels
./.config/Thunar
./.config/Thunar/accels.scm
./.config/qt6ct
./.config/qt6ct/qss
./.config/qt6ct/colors
./.config/qt6ct/qt6ct.conf
./.config/QtProject.conf
./.config/enchant
./.config/enchant/en_US.dic
./.config/enchant/en_US.exc
./.config/pulse
./.config/pulse/cookie
./.config/user-dirs.locale
./.config/user-dirs.dirs
./.config/xfce4
./.config/xfce4/desktop
./.config/xfce4/desktop/icons.screen0-1904x1029.rc
./.config/xfce4/desktop/icons.screen0-1702x827.rc
./.config/xfce4/desktop/icons.screen.latest.rc
./.config/xfce4/desktop/icons.screen0-1698x823.rc
./.config/xfce4/xfwm4
./.config/xfce4/panel
./.config/xfce4/panel/launcher-5
./.config/xfce4/panel/launcher-5/17332522771.desktop
./.config/xfce4/panel/genmon-15.rc
./.config/xfce4/panel/launcher-7
./.config/xfce4/panel/launcher-7/17332522775.desktop
./.config/xfce4/panel/launcher-7/17332522773.desktop
./.config/xfce4/panel/launcher-7/17332522774.desktop
./.config/xfce4/panel/launcher-6
./.config/xfce4/panel/launcher-6/17332522772.desktop
./.config/xfce4/xfconf
./.config/xfce4/xfconf/xfce-perchannel-xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xsettings.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-settings-manager.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/thunar.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-notifyd.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/ristretto.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-power-manager.xml
./.config/xfce4/xfce4-screenshooter
./.config/cherrytree
./.config/cherrytree/config.cfg
./.config/dconf
./.config/dconf/user
./.config/qterminal.org
./.config/qterminal.org/qterminal_bookmarks.xml
./.config/qterminal.org/qterminal.ini
./.config/ristretto
./.config/ristretto/accels.scm
./.profile
./.zsh_history
./.xsession-errors.old
./.java
./.java/.userPrefs
./.java/.userPrefs/burp
./.java/.userPrefs/burp/prefs.xml
./Public
./.viminfo
./.face
./Templates
./.bash_history
./.dmrc
./Videos
./.python_history
./.Xauthority
./Desktop
./Desktop/Java Apna College
./Desktop/Java Apna College/calculator.class
./Desktop/Java Apna College/calculator.java
./Desktop/Java Apna College/pattern3.java
./Desktop/Java Apna College/pattern5.java
./Desktop/Java Apna College/pattern1.class
./Desktop/Java Apna College/table.class
./Desktop/Java Apna College/pattern6.class
./Desktop/Java Apna College/pattern6.java
./Desktop/Java Apna College/pattern2.class
./Desktop/Java Apna College/table.java
./Desktop/Java Apna College/pattern5.class
./Desktop/Java Apna College/pattern4.java
./Desktop/Java Apna College/day.java
./Desktop/Java Apna College/pattern1.java
./Desktop/Java Apna College/pattern4.class
./Desktop/Java Apna College/prime.class
./Desktop/Java Apna College/pattern3.class
./Desktop/Java Apna College/prime.java
./Desktop/Java Apna College/pattern2.java
./Desktop/Java Apna College/day.class
./Desktop/Assembly Codes
./Desktop/Assembly Codes/License.asm
./Desktop/Assembly Codes/prog5.o
./Desktop/Assembly Codes/prog5
./Desktop/Assembly Codes/License.o
./Desktop/Assembly Codes/prog4.asm
./Desktop/Assembly Codes/prog1.o
./Desktop/Assembly Codes/prog3.o
./Desktop/Assembly Codes/prog1.asm
./Desktop/Assembly Codes/prog2
./Desktop/Assembly Codes/prog2.o
./Desktop/Assembly Codes/prog6.asm
./Desktop/Assembly Codes/prog7.o
./Desktop/Assembly Codes/prog5.asm
./Desktop/Assembly Codes/prog7
./Desktop/Assembly Codes/prog1
./Desktop/Assembly Codes/key.txt
./Desktop/Assembly Codes/prog6
./Desktop/Assembly Codes/prog6.o
./Desktop/Assembly Codes/prog7.asm
./Desktop/Assembly Codes/prog4
./Desktop/Assembly Codes/prog3.asm
./Desktop/Assembly Codes/prog3
./Desktop/Assembly Codes/1
./Desktop/Assembly Codes/prog2.asm
./Desktop/Assembly Codes/prog4.o
./Desktop/Assembly Codes/key
./Desktop/Assembly Codes/1.o
./Desktop/Assembly Codes/License
./Desktop/util.asm
./.zshrc
./.wget-hsts
./.local
./.local/state
./.local/state/lesshst
./.local/state/wireplumber
./.local/state/wireplumber/stream-properties
./.local/share
./.local/share/keyrings
./.local/share/keyrings/login.keyring
./.local/share/keyrings/user.keystore
./.local/share/gedit
./.local/share/gedit/gedit-metadata.xml
./.local/share/nano
./.local/share/nano/search_history
./.local/share/nautilus
./.local/share/nautilus/scripts
./.local/share/nautilus/scripts/Terminal
./.local/share/icc
./.local/share/recently-used.xbel
./.local/share/gvfs-metadata
./.local/share/gvfs-metadata/home
./.local/share/gvfs-metadata/home.IJVIY2
./.local/share/gvfs-metadata/home-f7d02a5d.log
./.local/share/ristretto
./.bash_logout
./Pictures
./Pictures/Screenshot_2024-12-30_11_41_28.png
./Pictures/wallpaperflare.com_wallpaper.jpg
./Pictures/mr robot.jpg
./Pictures/wallpaper1.jpg
./Music
./.sudo_as_admin_successful
./Downloads
./.bashrc
./.ICEauthority
./.bashrc.original
./.gnupg
./.gnupg/private-keys-v1.d
./.xsession-errors
./.cache
./.cache/gstreamer-1.0
./.cache/gstreamer-1.0/registry.x86_64.bin
./.cache/vmware
./.cache/vmware/drag_and_drop
./.cache/vmware/drag_and_drop/YSD9hX
./.cache/vmware/drag_and_drop/YSD9hX/arithmetic
./.cache/vmware/drag_and_drop/YSD9hX/print
./.cache/vmware/drag_and_drop/YSD9hX/input
./.cache/vmware/drag_and_drop/fmyyYy
./.cache/vmware/drag_and_drop/fmyyYy/Screenshot 2024-12-30 203558.png
./.cache/vmware/drag_and_drop/ituzNH
./.cache/vmware/drag_and_drop/ituzNH/Sem 4 fees.pdf
./.cache/vmware/drag_and_drop/GsDEp1
./.cache/vmware/drag_and_drop/GsDEp1/input.asm
./.cache/vmware/drag_and_drop/GsDEp1/print.asm
./.cache/vmware/drag_and_drop/GsDEp1/arithmetic.asm
./.cache/mesa_shader_cache
./.cache/mesa_shader_cache/marker
./.cache/mesa_shader_cache/index
./.cache/mesa_shader_cache/f1
./.cache/mesa_shader_cache/f1/327ed63bf76c91f80a00c6688850b0e977be54
./.cache/mesa_shader_cache/b9
./.cache/mesa_shader_cache/b9/6de62d00e2891a96ef4c53ec86d062eb23c2d6
./.cache/mesa_shader_cache/a8
./.cache/mesa_shader_cache/a8/378e6c9e1de42b5c44a8ffaeefe840ad38deca
./.cache/sessions
./.cache/xfce4
./.cache/xfce4/notifyd
./.cache/xfce4/notifyd/log.sqlite
./.cache/thumbnails
./.cache/thumbnails/normal
./.cache/thumbnails/normal/48a494c4390f3bb901e7df16d17d8c43.png
./.cache/thumbnails/normal/c2b968895383457007538c88c09b1ac7.png
./.cache/thumbnails/normal/e2fdfdc26c4fd4835c4f1eaa0b7ac1de.png
./.cache/thumbnails/normal/aed87a6c11932284869d1fddcd72fb9c.png
./.cache/thumbnails/normal/2f377eff7e40e531403b4aaf6e175acb.png
./.cache/thumbnails/normal/4132de79c204c8d4910e9a9c662f7fb1.png
./.cache/thumbnails/normal/88e2c122d9bf4f76174b13e36932e90e.png
./.cache/thumbnails/normal/1a508ee257f989f6d38a03cbb831d68b.png
./.cache/thumbnails/normal/4d1ea328510151a54ddc0927883efdc8.png
./.cache/thumbnails/normal/1d3ccd218d6bfe9b7e9052aadbc24391.png
./.cache/thumbnails/normal/a23c30347c949e21a11ad239b594170a.png
./.cache/thumbnails/normal/fe0ed1b54f5b04084cfe95ee9ed984ce.png
./.cache/thumbnails/normal/a0b1e18333b6371004e7cfcbb98a26bf.png
./.cache/thumbnails/normal/1221d65c09770c7cb6ee115a3074614a.png
./.cache/thumbnails/normal/89bd816daac783cf17d617a6d4654838.png
./.cache/thumbnails/normal/e84c2a05a014d4d5d5d6f749fbae5984.png
./.cache/thumbnails/normal/8d1b517797035e64b63c7a7e9e20a6c6.png
./.cache/thumbnails/normal/eeae94be04b2cf0d9308fa382c003021.png
./.cache/thumbnails/normal/9b83f3e5fac5e2bd0fe87a7220d188f4.png
./.cache/thumbnails/normal/70c19a02899ed095d80dfd1b74290e5f.png
./.cache/thumbnails/normal/3aad6a2ac28d1cc58a5ff5940bde213b.png
./.cache/thumbnails/normal/c525c41123e21d307ed6da51cca60492.png
./.cache/thumbnails/normal/cf25bcdb80a466597fa9a9105a762f42.png
./.cache/thumbnails/normal/5482658bfd333091c78545a760d5b4a4.png
./.cache/thumbnails/normal/a3ff4c9c514b83d45d3af88d6ce6302a.png
./.cache/thumbnails/normal/ca630105d2fed92d4d10091c48f23161.png
./.cache/thumbnails/normal/fe2ad13903a9a9e213267c131caad858.png
./.cache/thumbnails/normal/df3bac90a9b1d099569552dac22d35e4.png
./.cache/thumbnails/normal/d05989f8a5554fb0d728cc2e9ec5016f.png
./.cache/thumbnails/normal/a9c12fbdd54cb243262d00566956f847.png
./.cache/thumbnails/normal/9584bd82bda2a62c9660d322deefb3ac.png
./.cache/thumbnails/normal/72fd2d3ed260e249449c4cbb23a727d8.png
./.cache/thumbnails/normal/dd3a1b157ff1fc8154fd7a8b4eda552a.png
./.cache/thumbnails/normal/662c2b9049112edc35ed1ee179ebaf6e.png
./.cache/thumbnails/normal/8e63c2bfe6917da26203e2cc03df8dfa.png
./.cache/thumbnails/normal/35e6ee6cefc11342ca6ce97e4b90dc26.png
./.cache/thumbnails/normal/41c4637935b454fdb158e3ab90f02fac.png
./.cache/thumbnails/normal/32f5042ca722933e33f7f3da791a6e6d.png
./.cache/thumbnails/normal/8850bd86b94fb45ea44b92e7a0538bff.png
./.cache/thumbnails/normal/b6a00d211b4099c7db8404bd49102b7b.png
./.cache/thumbnails/normal/67b1cf61e4d46c42c4c65e0e87abaf68.png
./.cache/thumbnails/normal/01c518c27d7a534c54067335424b24c1.png
./.cache/thumbnails/normal/43f66ae0fdb2a9187dcf65c2a30dce19.png
./.cache/thumbnails/normal/924d97db4fd34729fd880161f28144e8.png
./.cache/thumbnails/normal/4d3fbfbee14464d696d9a11657b564d5.png
./.cache/thumbnails/normal/d026f0ffa555b950fa790d0abc89a013.png
./.cache/thumbnails/large
./.cache/thumbnails/large/eeae94be04b2cf0d9308fa382c003021.png
./.cache/thumbnails/large/9584bd82bda2a62c9660d322deefb3ac.png
./.cache/obexd
./.cache/zcompdump
```

## ```Finding Files in the Current Path```

Let's say I only want the files present in the current path using **find** command. To do that I need to mention the **type**.
```
┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]
└─$ find ./ -type f
./.config/powershell/Microsoft.PowerShell_profile.ps1
./.config/gtk-3.0/bookmarks
./.config/gedit/accels
./.config/qt5ct/qt5ct.conf
./.config/nautilus/scripts-accels
./.config/Thunar/accels.scm
./.config/qt6ct/qt6ct.conf
./.config/QtProject.conf
./.config/enchant/en_US.dic
./.config/enchant/en_US.exc
./.config/pulse/cookie
./.config/user-dirs.locale
./.config/user-dirs.dirs
./.config/xfce4/desktop/icons.screen0-1904x1029.rc
./.config/xfce4/desktop/icons.screen0-1702x827.rc
./.config/xfce4/desktop/icons.screen0-1698x823.rc
./.config/xfce4/panel/launcher-5/17332522771.desktop
./.config/xfce4/panel/genmon-15.rc
./.config/xfce4/panel/launcher-7/17332522775.desktop
./.config/xfce4/panel/launcher-7/17332522773.desktop
./.config/xfce4/panel/launcher-7/17332522774.desktop
./.config/xfce4/panel/launcher-6/17332522772.desktop
./.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xsettings.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/displays.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-desktop.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-settings-manager.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/thunar.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-notifyd.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/ristretto.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml
./.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-power-manager.xml
./.config/xfce4/xfce4-screenshooter
./.config/cherrytree/config.cfg
./.config/dconf/user
./.config/qterminal.org/qterminal_bookmarks.xml
./.config/qterminal.org/qterminal.ini
./.config/ristretto/accels.scm
./.profile
./.zsh_history
./.xsession-errors.old
./.java/.userPrefs/burp/prefs.xml
./.viminfo
./.face
./.bash_history
./.dmrc
./.python_history
./.Xauthority
./Desktop/Java Apna College/calculator.class
./Desktop/Java Apna College/calculator.java
./Desktop/Java Apna College/pattern3.java
./Desktop/Java Apna College/pattern5.java
./Desktop/Java Apna College/pattern1.class
./Desktop/Java Apna College/table.class
./Desktop/Java Apna College/pattern6.class
./Desktop/Java Apna College/pattern6.java
./Desktop/Java Apna College/pattern2.class
./Desktop/Java Apna College/table.java
./Desktop/Java Apna College/pattern5.class
./Desktop/Java Apna College/pattern4.java
./Desktop/Java Apna College/day.java
./Desktop/Java Apna College/pattern1.java
./Desktop/Java Apna College/pattern4.class
./Desktop/Java Apna College/prime.class
./Desktop/Java Apna College/pattern3.class
./Desktop/Java Apna College/prime.java
./Desktop/Java Apna College/pattern2.java
./Desktop/Java Apna College/day.class
./Desktop/Assembly Codes/License.asm
./Desktop/Assembly Codes/prog5.o
./Desktop/Assembly Codes/prog5
./Desktop/Assembly Codes/License.o
./Desktop/Assembly Codes/prog4.asm
./Desktop/Assembly Codes/prog1.o
./Desktop/Assembly Codes/prog3.o
./Desktop/Assembly Codes/prog1.asm
./Desktop/Assembly Codes/prog2
./Desktop/Assembly Codes/prog2.o
./Desktop/Assembly Codes/prog6.asm
./Desktop/Assembly Codes/prog7.o
./Desktop/Assembly Codes/prog5.asm
./Desktop/Assembly Codes/prog7
./Desktop/Assembly Codes/prog1
./Desktop/Assembly Codes/key.txt
./Desktop/Assembly Codes/prog6
./Desktop/Assembly Codes/prog6.o
./Desktop/Assembly Codes/prog7.asm
./Desktop/Assembly Codes/prog4
./Desktop/Assembly Codes/prog3.asm
./Desktop/Assembly Codes/prog3
./Desktop/Assembly Codes/1
./Desktop/Assembly Codes/prog2.asm
./Desktop/Assembly Codes/prog4.o
./Desktop/Assembly Codes/key
./Desktop/Assembly Codes/1.o
./Desktop/Assembly Codes/License
./Desktop/util.asm
./.zshrc
./.wget-hsts
./.local/state/lesshst
./.local/state/wireplumber/stream-properties
./.local/share/keyrings/login.keyring
./.local/share/keyrings/user.keystore
./.local/share/gedit/gedit-metadata.xml
./.local/share/nano/search_history
./.local/share/nautilus/scripts/Terminal
./.local/share/recently-used.xbel
./.local/share/gvfs-metadata/home
./.local/share/gvfs-metadata/home.IJVIY2
./.local/share/gvfs-metadata/home-f7d02a5d.log
./.bash_logout
./Pictures/Screenshot_2024-12-30_11_41_28.png
./Pictures/wallpaperflare.com_wallpaper.jpg
./Pictures/mr robot.jpg
./Pictures/wallpaper1.jpg
./.sudo_as_admin_successful
./.bashrc
./.ICEauthority
./.bashrc.original
./.xsession-errors
./.cache/gstreamer-1.0/registry.x86_64.bin
./.cache/vmware/drag_and_drop/YSD9hX/arithmetic
./.cache/vmware/drag_and_drop/YSD9hX/print
./.cache/vmware/drag_and_drop/YSD9hX/input
./.cache/vmware/drag_and_drop/fmyyYy/Screenshot 2024-12-30 203558.png
./.cache/vmware/drag_and_drop/ituzNH/Sem 4 fees.pdf
./.cache/vmware/drag_and_drop/GsDEp1/input.asm
./.cache/vmware/drag_and_drop/GsDEp1/print.asm
./.cache/vmware/drag_and_drop/GsDEp1/arithmetic.asm
./.cache/mesa_shader_cache/marker
./.cache/mesa_shader_cache/index
./.cache/mesa_shader_cache/f1/327ed63bf76c91f80a00c6688850b0e977be54
./.cache/mesa_shader_cache/b9/6de62d00e2891a96ef4c53ec86d062eb23c2d6
./.cache/mesa_shader_cache/a8/378e6c9e1de42b5c44a8ffaeefe840ad38deca
./.cache/xfce4/notifyd/log.sqlite
./.cache/thumbnails/normal/48a494c4390f3bb901e7df16d17d8c43.png
./.cache/thumbnails/normal/c2b968895383457007538c88c09b1ac7.png
./.cache/thumbnails/normal/e2fdfdc26c4fd4835c4f1eaa0b7ac1de.png
./.cache/thumbnails/normal/aed87a6c11932284869d1fddcd72fb9c.png
./.cache/thumbnails/normal/2f377eff7e40e531403b4aaf6e175acb.png
./.cache/thumbnails/normal/4132de79c204c8d4910e9a9c662f7fb1.png
./.cache/thumbnails/normal/88e2c122d9bf4f76174b13e36932e90e.png
./.cache/thumbnails/normal/1a508ee257f989f6d38a03cbb831d68b.png
./.cache/thumbnails/normal/4d1ea328510151a54ddc0927883efdc8.png
./.cache/thumbnails/normal/1d3ccd218d6bfe9b7e9052aadbc24391.png
./.cache/thumbnails/normal/a23c30347c949e21a11ad239b594170a.png
./.cache/thumbnails/normal/fe0ed1b54f5b04084cfe95ee9ed984ce.png
./.cache/thumbnails/normal/a0b1e18333b6371004e7cfcbb98a26bf.png
./.cache/thumbnails/normal/1221d65c09770c7cb6ee115a3074614a.png
./.cache/thumbnails/normal/89bd816daac783cf17d617a6d4654838.png
./.cache/thumbnails/normal/e84c2a05a014d4d5d5d6f749fbae5984.png
./.cache/thumbnails/normal/8d1b517797035e64b63c7a7e9e20a6c6.png
./.cache/thumbnails/normal/eeae94be04b2cf0d9308fa382c003021.png
./.cache/thumbnails/normal/9b83f3e5fac5e2bd0fe87a7220d188f4.png
./.cache/thumbnails/normal/70c19a02899ed095d80dfd1b74290e5f.png
./.cache/thumbnails/normal/3aad6a2ac28d1cc58a5ff5940bde213b.png
./.cache/thumbnails/normal/c525c41123e21d307ed6da51cca60492.png
./.cache/thumbnails/normal/cf25bcdb80a466597fa9a9105a762f42.png
./.cache/thumbnails/normal/5482658bfd333091c78545a760d5b4a4.png
./.cache/thumbnails/normal/a3ff4c9c514b83d45d3af88d6ce6302a.png
./.cache/thumbnails/normal/ca630105d2fed92d4d10091c48f23161.png
./.cache/thumbnails/normal/fe2ad13903a9a9e213267c131caad858.png
./.cache/thumbnails/normal/df3bac90a9b1d099569552dac22d35e4.png
./.cache/thumbnails/normal/d05989f8a5554fb0d728cc2e9ec5016f.png
./.cache/thumbnails/normal/a9c12fbdd54cb243262d00566956f847.png
./.cache/thumbnails/normal/9584bd82bda2a62c9660d322deefb3ac.png
./.cache/thumbnails/normal/72fd2d3ed260e249449c4cbb23a727d8.png
./.cache/thumbnails/normal/dd3a1b157ff1fc8154fd7a8b4eda552a.png
./.cache/thumbnails/normal/662c2b9049112edc35ed1ee179ebaf6e.png
./.cache/thumbnails/normal/8e63c2bfe6917da26203e2cc03df8dfa.png
./.cache/thumbnails/normal/35e6ee6cefc11342ca6ce97e4b90dc26.png
./.cache/thumbnails/normal/41c4637935b454fdb158e3ab90f02fac.png
./.cache/thumbnails/normal/32f5042ca722933e33f7f3da791a6e6d.png
./.cache/thumbnails/normal/8850bd86b94fb45ea44b92e7a0538bff.png
./.cache/thumbnails/normal/b6a00d211b4099c7db8404bd49102b7b.png
./.cache/thumbnails/normal/67b1cf61e4d46c42c4c65e0e87abaf68.png
./.cache/thumbnails/normal/01c518c27d7a534c54067335424b24c1.png
./.cache/thumbnails/normal/43f66ae0fdb2a9187dcf65c2a30dce19.png
./.cache/thumbnails/normal/924d97db4fd34729fd880161f28144e8.png
./.cache/thumbnails/normal/4d3fbfbee14464d696d9a11657b564d5.png
./.cache/thumbnails/normal/d026f0ffa555b950fa790d0abc89a013.png
./.cache/thumbnails/large/eeae94be04b2cf0d9308fa382c003021.png
./.cache/thumbnails/large/9584bd82bda2a62c9660d322deefb3ac.png
./.cache/zcompdump
```

## ```Finding Directories in the Current Path```

Let's say I only want the directories present in the current path using **find** command. To do that I need to mention the **type**.

```
┌──(kali㉿kali)-[~]
└─$ find ./ -type d
./
./Documents
./.config
./.config/powershell
./.config/gtk-3.0
./.config/gedit
./.config/qt5ct
./.config/qt5ct/qss
./.config/qt5ct/colors
./.config/nautilus
./.config/Thunar
./.config/qt6ct
./.config/qt6ct/qss
./.config/qt6ct/colors
./.config/enchant
./.config/pulse
./.config/xfce4
./.config/xfce4/desktop
./.config/xfce4/xfwm4
./.config/xfce4/panel
./.config/xfce4/panel/launcher-5
./.config/xfce4/panel/launcher-7
./.config/xfce4/panel/launcher-6
./.config/xfce4/xfconf
./.config/xfce4/xfconf/xfce-perchannel-xml
./.config/cherrytree
./.config/dconf
./.config/qterminal.org
./.config/ristretto
./.java
./.java/.userPrefs
./.java/.userPrefs/burp
./Public
./Templates
./Videos
./Desktop
./Desktop/Java Apna College
./Desktop/Assembly Codes
./.local
./.local/state
./.local/state/wireplumber
./.local/share
./.local/share/keyrings
./.local/share/gedit
./.local/share/nano
./.local/share/nautilus
./.local/share/nautilus/scripts
./.local/share/icc
./.local/share/gvfs-metadata
./.local/share/ristretto
./Pictures
./Music
./Downloads
./.gnupg
./.gnupg/private-keys-v1.d
./.cache
./.cache/gstreamer-1.0
./.cache/vmware
./.cache/vmware/drag_and_drop
./.cache/vmware/drag_and_drop/YSD9hX
./.cache/vmware/drag_and_drop/fmyyYy
./.cache/vmware/drag_and_drop/ituzNH
./.cache/vmware/drag_and_drop/GsDEp1
./.cache/mesa_shader_cache
./.cache/mesa_shader_cache/f1
./.cache/mesa_shader_cache/b9
./.cache/mesa_shader_cache/a8
./.cache/sessions
./.cache/xfce4
./.cache/xfce4/notifyd
./.cache/thumbnails
./.cache/thumbnails/normal
./.cache/thumbnails/large
./.cache/obexd
```

## ```Finding Files by specifying name```

Information required for better search results using **find** command.

-   path/location 
-   type (file/directory)
-   file/directory name

Sometimes we don't have permission and thoses searches face "**Permission Denied**" and the rest get displayed.
```
┌──(kali㉿kali)-[~]
└─$ sudo find / -type f -name proxychains
/var/lib/dpkg/alternatives/proxychains
find: ‘/run/user/1000/gvfs’: Permission denied
```

Finding directories matching the word "**kali**".
You can use the **-iname** instead of **-name** in **find** command to ommit case sensitive searches for a file/directory.
```
┌──(kali㉿kali)-[~]
└─$ sudo find / -type d -name kali
/var/lib/lightdm/data/kali
/home/kali
/usr/share/plasma/desktoptheme/kali
/usr/share/backgrounds/kali
/usr/share/plymouth/themes/kali
/usr/share/grub/themes/kali
/boot/grub/themes/kali
find: ‘/run/user/1000/gvfs’: Permission denied
```

We can use **piping** along with **find** command to search for particular file extensions to narrow down our search. Let's say I want to find all the **.conf files in the /etc** directory.
```
┌──(kali㉿kali)-[~]
└─$ sudo find /etc -type f -name "*.conf" | grep proxychains
/etc/proxychains4.conf
```

## ```Finding Files based on Size```

We are going to find files based on their file size using **find** command. b = bytes M = megabytes .etc.

The below command searches for files in the entire Linux System having more than 20MB file size.
```
┌──(kali㉿kali)-[~]
└─$ sudo find / -type f -size +20M
/proc/kcore
find: ‘/proc/64500/task/64500/fdinfo/5’: No such file or directory
find: ‘/proc/64500/fdinfo/6’: No such file or directory
/var/log/journal/30e662c5c81d4191bd2444a79c97d2e0/system@74b284fadfa44455bb9b3ea0691303f6-0000000000000001-000628623cac546e.journal
/var/lib/apt/lists/http.kali.org_kali_dists_kali-last-snapshot_main_Contents-amd64.lz4
/var/lib/apt/lists/http.kali.org_kali_dists_kali-last-snapshot_main_binary-amd64_Packages
/var/lib/mysql/ib_logfile0
/var/cache/apt/pkgcache.bin
/var/cache/apt/srcpkgcache.bin
/usr/libexec/gcc/x86_64-linux-gnu/13/cc1plus
/usr/libexec/gcc/x86_64-linux-gnu/13/lto1
/usr/libexec/gcc/x86_64-linux-gnu/13/cc1
/usr/sbin/msrtool
/usr/sbin/mariadbd
/usr/lib/gophish/static/db/geolite2-city.mmdb
/usr/lib/firefox-esr/browser/omni.ja
/usr/lib/firefox-esr/libxul.so
/usr/lib/firefox-esr/omni.ja
/usr/lib/llvm-16/lib/libclang-cpp.so.16
/usr/lib/llvm-16/bin/llvm-exegesis
/usr/lib/oracle/19.6/client64/lib/libclntsh.so.19.1
/usr/lib/oracle/19.6/client64/lib/libociei.so
/usr/lib/gcc/x86_64-w64-mingw32/13-win32/libstdc++-6.dll
/usr/lib/gcc/x86_64-w64-mingw32/13-win32/lto1
/usr/lib/gcc/x86_64-w64-mingw32/13-win32/cc1
/usr/lib/gcc/i686-w64-mingw32/13-win32/libstdc++-6.dll
/usr/lib/gcc/i686-w64-mingw32/13-win32/lto1
/usr/lib/gcc/i686-w64-mingw32/13-win32/cc1
/usr/lib/jvm/java-21-openjdk-amd64/lib/modules
/usr/lib/jvm/java-21-openjdk-amd64/lib/server/libjvm.so
/usr/lib/jvm/java-21-openjdk-amd64/jmods/java.base.jmod
/usr/lib/jvm/java-23-openjdk-amd64/lib/modules
/usr/lib/jvm/java-23-openjdk-amd64/lib/server/libjvm.so
/usr/lib/jvm/java-17-openjdk-amd64/lib/modules
/usr/lib/jvm/java-17-openjdk-amd64/lib/server/libjvm.so
/usr/lib/chromium/chromium
/usr/lib/x86_64-linux-gnu/libclang-16.so.16.0.6
/usr/lib/x86_64-linux-gnu/libgdal.so.34.3.8.5
/usr/lib/x86_64-linux-gnu/libicudata.so.72.1
/usr/lib/x86_64-linux-gnu/libwebkit2gtk-4.1.so.0.13.6
/usr/lib/x86_64-linux-gnu/libgs.so.10.03
/usr/lib/x86_64-linux-gnu/dri/nouveau_dri.so
/usr/lib/x86_64-linux-gnu/dri/radeonsi_dri.so
/usr/lib/x86_64-linux-gnu/dri/r600_dri.so
/usr/lib/x86_64-linux-gnu/dri/swrast_dri.so
/usr/lib/x86_64-linux-gnu/dri/d3d12_dri.so
/usr/lib/x86_64-linux-gnu/dri/crocus_dri.so
/usr/lib/x86_64-linux-gnu/dri/kms_swrast_dri.so
/usr/lib/x86_64-linux-gnu/dri/vmwgfx_dri.so
/usr/lib/x86_64-linux-gnu/dri/virtio_gpu_dri.so
/usr/lib/x86_64-linux-gnu/dri/r300_dri.so
/usr/lib/x86_64-linux-gnu/dri/i915_dri.so
/usr/lib/x86_64-linux-gnu/dri/iris_dri.so
/usr/lib/x86_64-linux-gnu/dri/zink_dri.so
/usr/lib/x86_64-linux-gnu/libLLVM-16.so.1
/usr/lib/x86_64-linux-gnu/libicudata.a
/usr/lib/x86_64-linux-gnu/libLLVM-17.so.1
/usr/lib/x86_64-linux-gnu/libz3.so.4
/usr/lib/x86_64-linux-gnu/libwireshark.so.17.0.5
/usr/lib/x86_64-linux-gnu/libclang-17.so.17
/usr/lib/x86_64-linux-gnu/libQt5WebKit.so.5.212.0
/usr/lib/x86_64-linux-gnu/libjavascriptcoregtk-4.1.so.0.5.6
/usr/lib/llvm-17/lib/libclang-cpp.so.17
/usr/lib/llvm-17/bin/llvm-exegesis
/usr/lib/python3/dist-packages/playwright/driver/node
/usr/bin/amass
/usr/bin/muraster
/usr/bin/x86_64-w64-mingw32-lto-dump-win32
/usr/bin/x86_64-linux-gnu-lto-dump-13
/usr/bin/i686-w64-mingw32-lto-dump-win32
/usr/bin/mutool
/usr/share/metasploit-framework/vendor/bundle/ruby/3.1.0/cache/metasploit-payloads-2.0.166.gem
/usr/share/metasploit-framework/vendor/bundle/ruby/3.1.0/cache/metasploit_payloads-mettle-1.0.31.gem
/usr/share/burpsuite/burpsuite.jar
/usr/share/wordlists/rockyou.txt.gz
/usr/share/dotnet/sdk/6.0.400/FSharp/FSharp.Compiler.Service.dll
/usr/share/pocketsphinx/model/en-us/en-us.lm.bin
/sys/devices/pci0000:00/0000:00:0f.0/resource1
/sys/devices/pci0000:00/0000:00:0f.0/resource1_wc
/swapfile
/boot/initrd.img-6.8.11-amd64
find: ‘/run/user/1000/gvfs’: Permission denied
```

## ```perm with find command```


**perm** is used with **find** command to find files having particular permissions set on them. To demonstrate this understand the scenario.

Let's say I create a file name **file1.txt**. Give **read** permissions to user and no access/permissions to groups and others.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch file1.txt

┌──(kali㉿kali)-[~/Desktop]
└─$ chmod 400 file1.txt 
```

Now let's use **perm** in **find** command to demonstrate the usage.

```
┌──(kali㉿kali)-[~/Desktop]
└─$ sudo find ./ -type f -perm 400 
./file1.txt
```