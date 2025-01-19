![alt text](Linux.jpg)

# Service and Process Management in Linux

In this section we are going to learn about Service and Process Management using Linux.

## ```top```

**top** is like task manager in windows showing us all the processses and applications and services running in our Linux system executed by users or the root.

A small screenshot giving us the preview of **top** utitlity.
```                                                          
top - 07:05:58 up 26 min,  2 users,  load average: 0.37, 0.19, 0.12
Tasks: 202 total,   1 running, 201 sleeping,   0 stopped,   0 zombie
%Cpu(s):  1.6 us,  1.6 sy,  0.0 ni, 96.8 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st 
MiB Mem :   5985.9 total,   4787.6 free,    795.2 used,    641.2 buff/cache     
MiB Swap:   1024.0 total,   1024.0 free,      0.0 used.   5190.7 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                                           
    979 root      20   0  392756 112848  56272 S  10.3   1.8   0:23.55 Xorg                                                                                              
   1375 kali      20   0  464888 107580  86728 S   1.3   1.8   0:03.80 qterminal                                                                                         
    580 root      20   0  243896   9088   7808 S   0.7   0.1   0:05.49 vmtoolsd                                                                                          
   1260 kali      20   0 1264128 119356  79312 S   0.7   1.9   0:06.54 xfwm4                                                                                             
   1461 kali      20   0  212652  38188  29488 S   0.7   0.6   0:03.96 vmtoolsd                                                                                          
   1313 kali      20   0  300352  60896  18688 S   0.3   1.0   0:04.44 panel-13-cpugra                                                                                   
   1315 kali      20   0  337792  27056  20068 S   0.3   0.4   0:04.33 panel-15-
```

## ```htop```

**htop** utility is same as **top** utility but has various features and better UI. We can kill a particular process, search for a particular process or task and shows us realtime usage and consumption of resources of memory and other stuff in the Linux system.

## ```free```

**free** command gives us information about how much RAM is used and how much is free. We can use the **-h** switch to see the output by **free** command in human readable form.
```
┌──(kali㉿kali)-[~]
└─$ free -h
               total        used        free      shared  buff/cache   available
Mem:           5.8Gi       803Mi       4.7Gi       9.0Mi       645Mi       5.1Gi
Swap:          1.0Gi          0B       1.0Gi
```

## ```ps aux```

**ps aux** command displays all processes running on the current shell of the user. **ps aux** gives us a snapshot of the current running processes but not in realtime unlike **top** or **htop** command.
```
┌──(kali㉿kali)-[~]
└─$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.2  22448 13548 ?        Ss   06:39   0:02 /sbin/init splash
root           2  0.0  0.0      0     0 ?        S    06:39   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        S    06:39   0:00 [pool_workqueue_release]
root           4  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-rcu_g]
root           5  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-rcu_p]
root           6  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-slub_]
root           7  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-netns]
root           9  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/0:0H-events_highpri]
root          11  0.0  0.0      0     0 ?        I    06:39   0:00 [kworker/u64:0-floppy]
root          12  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-mm_pe]
root          13  0.0  0.0      0     0 ?        I    06:39   0:00 [rcu_tasks_kthread]
root          14  0.0  0.0      0     0 ?        I    06:39   0:00 [rcu_tasks_rude_kthread]
root          15  0.0  0.0      0     0 ?        I    06:39   0:00 [rcu_tasks_trace_kthread]
root          16  0.0  0.0      0     0 ?        S    06:39   0:00 [ksoftirqd/0]
root          17  0.0  0.0      0     0 ?        I    06:39   0:01 [rcu_preempt]
root          18  0.0  0.0      0     0 ?        S    06:39   0:00 [migration/0]
root          19  0.0  0.0      0     0 ?        S    06:39   0:00 [idle_inject/0]
root          20  0.0  0.0      0     0 ?        S    06:39   0:00 [cpuhp/0]
root          21  0.0  0.0      0     0 ?        S    06:39   0:00 [cpuhp/1]
root          22  0.0  0.0      0     0 ?        S    06:39   0:00 [idle_inject/1]
root          23  0.0  0.0      0     0 ?        S    06:39   0:00 [migration/1]
root          24  0.0  0.0      0     0 ?        S    06:39   0:00 [ksoftirqd/1]
root          26  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/1:0H-events_highpri]
root          27  0.0  0.0      0     0 ?        S    06:39   0:00 [cpuhp/2]
root          28  0.0  0.0      0     0 ?        S    06:39   0:00 [idle_inject/2]
root          29  0.0  0.0      0     0 ?        S    06:39   0:00 [migration/2]
root          30  0.0  0.0      0     0 ?        S    06:39   0:00 [ksoftirqd/2]
root          32  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/2:0H-kblockd]
root          33  0.0  0.0      0     0 ?        S    06:39   0:00 [cpuhp/3]
root          34  0.0  0.0      0     0 ?        S    06:39   0:00 [idle_inject/3]
root          35  0.0  0.0      0     0 ?        S    06:39   0:00 [migration/3]
root          36  0.0  0.0      0     0 ?        S    06:39   0:00 [ksoftirqd/3]
root          38  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/3:0H-events_highpri]
root          40  0.0  0.0      0     0 ?        I    06:39   0:00 [kworker/u66:0-events_unbound]
root          42  0.0  0.0      0     0 ?        I    06:39   0:00 [kworker/u66:1-writeback]
root          45  0.0  0.0      0     0 ?        S    06:39   0:00 [kdevtmpfs]
root          46  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-inet_]
root          47  0.0  0.0      0     0 ?        I    06:39   0:02 [kworker/u65:1-events_unbound]
root          48  0.0  0.0      0     0 ?        S    06:39   0:00 [kauditd]
root          49  0.0  0.0      0     0 ?        I    06:39   0:00 [kworker/1:1-events]
root          52  0.0  0.0      0     0 ?        S    06:39   0:00 [khungtaskd]
root          53  0.0  0.0      0     0 ?        S    06:39   0:00 [oom_reaper]
root          55  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-write]
root          56  0.0  0.0      0     0 ?        S    06:39   0:00 [kcompactd0]
root          57  0.0  0.0      0     0 ?        SN   06:39   0:00 [ksmd]
root          58  0.0  0.0      0     0 ?        SN   06:39   0:00 [khugepaged]
root          59  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-kinte]
root          60  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-kbloc]
root          61  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-blkcg]
root          62  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/9-acpi]
root          64  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-tpm_d]
root          65  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-edac-]
root          66  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-devfr]
root          68  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/1:1H-kblockd]
root          69  0.0  0.0      0     0 ?        S    06:39   0:00 [kswapd0]
root          76  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-kthro]
root          78  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/24-pciehp]
root          79  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/25-pciehp]
root          80  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/26-pciehp]
root          81  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/27-pciehp]
root          82  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/28-pciehp]
root          83  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/29-pciehp]
root          84  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/30-pciehp]
root          85  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/31-pciehp]
root          86  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/32-pciehp]
root          87  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/33-pciehp]
root          88  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/34-pciehp]
root          89  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/35-pciehp]
root          90  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/36-pciehp]
root          91  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/37-pciehp]
root          92  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/38-pciehp]
root          93  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/39-pciehp]
root          94  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/40-pciehp]
root          95  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/41-pciehp]
root          96  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/42-pciehp]
root          97  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/43-pciehp]
root          98  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/44-pciehp]
root          99  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/45-pciehp]
root         100  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/46-pciehp]
root         101  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/47-pciehp]
root         102  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/48-pciehp]
root         103  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/49-pciehp]
root         104  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/50-pciehp]
root         105  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/51-pciehp]
root         106  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/52-pciehp]
root         107  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/53-pciehp]
root         108  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/54-pciehp]
root         109  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/55-pciehp]
root         110  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-acpi_]
root         111  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-mld]
root         112  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-ipv6_]
root         117  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-kstrp]
root         121  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/u67:0]
root         122  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/u68:0]
root         123  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/u69:0-ttm]
root         128  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-crypt]
root         211  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/3:1H-kblockd]
root         212  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/0:1H-kblockd]
root         240  0.0  0.0      0     0 ?        I    06:39   0:00 [kworker/u64:1-ext4-rsv-conversion]
root         241  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-ata_s]
root         244  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-mpt_p]
root         245  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-mpt/0]
root         250  0.0  0.0      0     0 ?        S    06:39   0:00 [scsi_eh_0]
root         251  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-scsi_]
root         252  0.0  0.0      0     0 ?        S    06:39   0:00 [scsi_eh_1]
root         253  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-scsi_]
root         254  0.0  0.0      0     0 ?        I    06:39   0:00 [kworker/u65:4-flush-8:0]
root         271  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/16-vmwgfx]
root         272  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-ttm]
root         273  0.0  0.0      0     0 ?        S    06:39   0:00 [scsi_eh_2]
root         274  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-scsi_]
root         311  0.0  0.0      0     0 ?        S    06:39   0:00 [jbd2/sda1-8]
root         312  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-ext4-]
root         354  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/56-vmw_vmci]
root         355  0.0  0.0      0     0 ?        S    06:39   0:00 [irq/57-vmw_vmci]
root         371  0.0  0.7  79948 43520 ?        Ss   06:39   0:00 /usr/lib/systemd/systemd-journald
root         392  0.0  0.0 152356  1548 ?        Ssl  06:39   0:00 vmware-vmblock-fuse /run/vmblock-fuse -o rw,subtype=vmware-vmblock,default_permissions,allow_other,dev
root         400  0.0  0.1  30256  8020 ?        Ss   06:39   0:00 /usr/lib/systemd/systemd-udevd
root         432  0.0  0.0      0     0 ?        S    06:39   0:00 [psimon]
root         571  0.0  0.1   8356  6408 ?        Ss   06:39   0:00 /usr/sbin/haveged --Foreground --verbose=1
root         580  0.3  0.1 243896  9088 ?        Ssl  06:39   0:12 /usr/bin/vmtoolsd
root         595  0.0  0.1 308512  7248 ?        Ssl  06:39   0:00 /usr/libexec/accounts-daemon
message+     596  0.0  0.0   8288  5120 ?        Ss   06:39   0:01 /usr/bin/dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-on
polkitd      599  0.0  0.1 382092  9772 ?        Ssl  06:39   0:01 /usr/lib/polkit-1/polkitd --no-debug
root         600  0.0  0.1  17920  8576 ?        Ss   06:39   0:00 /usr/lib/systemd/systemd-logind
root         617  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-rpcio]
root         621  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/R-xprti]
root         633  0.0  0.0   6736  2560 ?        Ss   06:39   0:00 /usr/sbin/cron -f
root         676  0.0  0.3 333548 19668 ?        Ssl  06:39   0:00 /usr/sbin/NetworkManager --no-daemon
root         710  0.0  0.1 389832 11472 ?        Ssl  06:39   0:00 /usr/sbin/ModemManager
root         746  0.0  0.0      0     0 ?        I<   06:39   0:00 [kworker/u69:1]
root         953  0.0  0.1 380768  7148 ?        SLsl 06:39   0:00 /usr/sbin/lightdm
root         979  2.7  2.0 405636 123864 tty7    Rsl+ 06:39   1:39 /usr/lib/xorg/Xorg :0 -seat seat0 -auth /var/run/lightdm/root/:0 -nolisten tcp vt7 -novtswitch
root         981  0.0  0.0   6988  2304 tty1     Ss+  06:39   0:00 /sbin/agetty -o -p -- \u --noclear - linux
root        1003  0.0  0.0      0     0 ?        S    06:39   0:00 [psimon]
rtkit       1030  0.0  0.0  20324  2816 ?        SNsl 06:39   0:00 /usr/libexec/rtkit-daemon
root        1113  0.0  0.1 236520  9528 ?        Sl   06:49   0:00 lightdm --session-child 13 24
kali        1121  0.0  0.1  21144 11904 ?        Ss   06:49   0:00 /usr/lib/systemd/systemd --user
kali        1122  0.0  0.0  22076  3504 ?        S    06:49   0:00 (sd-pam)
kali        1138  0.0  0.2 110012 14376 ?        S<sl 06:49   0:00 /usr/bin/pipewire
kali        1139  0.0  0.0  84660  5504 ?        Ssl  06:49   0:00 /usr/bin/pipewire -c filter-chain.conf
kali        1141  0.0  0.5 642140 33648 ?        S<sl 06:49   0:00 /usr/bin/wireplumber
kali        1142  0.0  0.1  99040  8960 ?        S<sl 06:49   0:00 /usr/bin/pipewire-pulse
kali        1143  0.0  0.1 313680  9728 ?        SLsl 06:49   0:00 /usr/bin/gnome-keyring-daemon --foreground --components=pkcs11,secrets --control-directory=/run/user/1
kali        1145  0.0  0.0   7344  4992 ?        Ss   06:49   0:00 /usr/bin/dbus-daemon --session --address=systemd: --nofork --nopidfile --systemd-activation --syslog-o
kali        1167  0.0  0.3 337164 24260 ?        Ssl  06:49   0:00 xfce4-session
kali        1216  0.0  0.0   9912  1424 ?        Ss   06:49   0:00 /usr/bin/ssh-agent x-session-manager
kali        1226  0.0  0.1 380804  7296 ?        Ssl  06:49   0:00 /usr/libexec/at-spi-bus-launcher
kali        1233  0.0  0.0   6972  4224 ?        S    06:49   0:00 /usr/bin/dbus-daemon --config-file=/usr/share/defaults/at-spi2/accessibility.conf --nofork --print-add
kali        1245  0.0  0.1 233940  7424 ?        Sl   06:49   0:00 /usr/libexec/at-spi2-registryd --use-gnome-session
kali        1258  0.0  0.0  81648  3456 ?        SLs  06:49   0:00 /usr/bin/gpg-agent --supervised
kali        1260  0.5  1.9 1266384 121148 ?      Sl   06:49   0:18 xfwm4 --display :0.0 --sm-client-id 2f9c5b8ee-75e9-456b-aa1f-73cfa06b07d4
kali        1264  0.0  0.1 312336  7424 ?        Ssl  06:49   0:00 /usr/libexec/gvfsd
kali        1270  0.0  0.1 457464  6912 ?        Sl   06:49   0:00 /usr/libexec/gvfsd-fuse /run/user/1000/gvfs -f
kali        1290  0.0  0.4 301332 26968 ?        Sl   06:49   0:00 xfsettingsd --display :0.0 --sm-client-id 2bf5fd250-d36f-42e9-9c88-d50d6d38f3c1
kali        1294  0.0  0.6 532244 40948 ?        Sl   06:49   0:00 xfce4-panel --display :0.0 --sm-client-id 23aefb912-45df-4e2b-93b4-02204b5c75a2
kali        1299  0.0  0.3 410696 23816 ?        Sl   06:49   0:00 Thunar --sm-client-id 2d8536a03-707a-4f99-983f-c7c9ef6b5b82 --daemon
kali        1305  0.0  0.8 472768 55032 ?        Sl   06:49   0:01 xfdesktop --display :0.0 --sm-client-id 256c02157-8ef7-4fd4-8366-626318588703
kali        1306  0.0  0.6 531460 41984 ?        Sl   06:49   0:00 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libwhi
kali        1313  0.4  0.9 300352 60896 ?        Sl   06:49   0:13 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libcpu
kali        1314  0.0  0.3 409508 24128 ?        Sl   06:49   0:00 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libsys
kali        1315  0.4  0.4 337792 27056 ?        Sl   06:49   0:12 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libgen
kali        1316  0.0  0.6 456564 40824 ?        Sl   06:49   0:00 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libpul
kali        1317  0.0  0.6 456504 37920 ?        Sl   06:49   0:00 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libnot
kali        1318  0.0  0.6 383320 38556 ?        Sl   06:49   0:02 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libxfc
kali        1320  0.0  0.6 383172 38700 ?        Sl   06:49   0:00 /usr/lib/x86_64-linux-gnu/xfce4/panel/wrapper-2.0 /usr/lib/x86_64-linux-gnu/xfce4/panel/plugins/libact
root        1349  0.0  0.1 316584  9600 ?        Ssl  06:49   0:01 /usr/libexec/upowerd
kali        1362  0.0  0.3 406388 19200 ?        Ssl  06:49   0:00 /usr/lib/x86_64-linux-gnu/xfce4/notifyd/xfce4-notifyd
kali        1375  0.4  1.7 465008 107836 ?       Sl   06:49   0:12 /usr/bin/qterminal -session 2bdf89e6d-ace0-49d3-b914-31625e1df949_1736786565_924687
kali        1376  0.0  0.3 262096 23312 ?        Sl   06:49   0:00 xfce4-power-manager --restart --sm-client-id 25b6eb672-c34f-4c3b-a342-582614224ca0
root        1398  0.0  0.0      0     0 ?        I    06:49   0:00 [kworker/u66:2]
kali        1403  0.0  0.1 308052  6144 ?        Sl   06:49   0:00 /usr/libexec/geoclue-2.0/demos/agent
kali        1404  0.0  0.7 619028 45008 ?        Sl   06:49   0:00 nm-applet
kali        1411  0.0  0.2 255960 15744 ?        Sl   06:49   0:00 /usr/libexec/polkit-mate-authentication-agent-1
kali        1417  0.0  0.5  61060 36704 ?        S    06:49   0:00 /usr/bin/python3 /usr/share/system-config-printer/applet.py
kali        1418  0.0  0.0  12712  1708 ?        Ssl  06:49   0:00 xcape -e Super_L Control_L Escape
kali        1420  0.0  0.2 425676 12800 ?        Ssl  06:49   0:00 /usr/libexec/gvfs-udisks2-volume-monitor
root        1448  0.0  0.2 468640 13160 ?        Ssl  06:49   0:00 /usr/libexec/udisks2/udisksd
kali        1459  0.0  0.0 230460  5760 ?        Ssl  06:49   0:00 /usr/libexec/dconf-service
kali        1461  0.3  0.6 212652 38188 ?        Sl   06:49   0:10 /usr/bin/vmtoolsd -n vmusr --blockFd 3
kali        1462  0.0  0.1 922384  8704 ?        Sl   06:49   0:00 xiccd
kali        1468  0.0  0.4 411248 27812 ?        Sl   06:49   0:00 light-locker
kali        1470  0.0  0.8 515672 52592 ?        Sl   06:49   0:00 /usr/bin/python3 /usr/bin/blueman-applet
colord      1498  0.0  0.2 315436 13608 ?        Ssl  06:49   0:00 /usr/libexec/colord
kali        1557  0.0  0.1 388724  8192 ?        Ssl  06:49   0:00 /usr/libexec/gvfs-afc-volume-monitor
kali        1572  0.0  0.1 307604  6144 ?        Ssl  06:49   0:00 /usr/libexec/gvfs-mtp-volume-monitor
kali        1585  0.0  0.0   9176  5888 pts/0    Ss   06:49   0:00 /usr/bin/bash
kali        1589  0.0  0.1 307516  6144 ?        Ssl  06:49   0:00 /usr/libexec/gvfs-goa-volume-monitor
kali        1599  0.0  0.1 308568  6656 ?        Ssl  06:49   0:00 /usr/libexec/gvfs-gphoto2-volume-monitor
kali        1629  0.0  0.1 533672  8832 ?        Sl   06:49   0:00 /usr/libexec/gvfsd-trash --spawner :1.21 /org/gtk/gvfs/exec_spaw/0
kali        1645  0.0  0.1 234092  6144 ?        Ssl  06:49   0:00 /usr/libexec/gvfsd-metadata
kali        1666  0.0  0.1  46720  7552 ?        Ss   06:49   0:00 /usr/libexec/bluetooth/obexd
root        1720  0.0  0.0      0     0 ?        I    06:49   0:00 [kworker/u65:2-events_unbound]
root        1723  0.0  0.0      0     0 ?        I    06:49   0:01 [kworker/0:3-events_power_efficient]
root        1804  0.0  0.0      0     0 ?        I<   06:49   0:00 [kworker/2:2H]
root        4156  0.0  0.0      0     0 ?        I    06:54   0:01 [kworker/2:2-events]
root        4190  0.0  0.0      0     0 ?        I    06:54   0:00 [kworker/3:0-events]
root        4191  0.0  0.0      0     0 ?        I    06:54   0:01 [kworker/3:3-events]
root       11317  0.0  0.0      0     0 ?        I    07:09   0:00 [kworker/2:0-rcu_par_gp]
root       11889  0.0  0.0      0     0 ?        I    07:10   0:00 [kworker/1:0-events]
root       19114  0.0  0.0      0     0 ?        I    07:25   0:00 [kworker/0:0-rcu_gp]
kali       25831  0.0  0.1 307280  6144 ?        Sl   07:38   0:00 /usr/lib/x86_64-linux-gnu/xfce4/xfconf/xfconfd
root       25914  0.0  0.0      0     0 ?        I    07:38   0:00 [kworker/2:1]
root       25916  0.0  0.0      0     0 ?        I    07:38   0:00 [kworker/0:1-rcu_par_gp]
root       25935  0.0  0.0      0     0 ?        I    07:38   0:00 [kworker/3:1-cgroup_destroy]
root       25936  0.0  0.0      0     0 ?        I    07:38   0:00 [kworker/1:2]
root       25943  0.0  0.0      0     0 ?        I    07:38   0:00 [kworker/3:2-cgroup_destroy]
root       26454  0.3  0.1 313060  8960 ?        Ssl  07:39   0:00 /usr/libexec/nm-dispatcher
kali       26501  100  0.0   8376  3840 pts/0    R+   07:40   0:00 ps aux
```

## ```systemctl```

**systemctl** command is used to start, display status , kill/end a process or service. You might need **sudo privileges** to start/display/end certain process or services.

- ### ```starting a service```
    ```
    ┌──(kali㉿kali)-[~]
    └─$ sudo systemctl start tor
    ```

- ### ```Checking service status```
    ```
    ┌──(kali㉿kali)-[~]
    └─$ sudo systemctl status tor
    ● tor.service - Anonymizing overlay network for TCP (multi-instance-master)
        Loaded: loaded (/usr/lib/systemd/system/tor.service; disabled; preset: disabled)
        Active: active (exited) since Sun 2025-01-19 07:47:35 EST; 7s ago
    Invocation: 63eca53ea3374e1dbec9b749ac979e36
        Process: 30618 ExecStart=/bin/true (code=exited, status=0/SUCCESS)
    Main PID: 30618 (code=exited, status=0/SUCCESS)
    ```

- ### ```Stop service```
    ```
    ┌──(kali㉿kali)-[~]
    └─$ sudo systemctl stop tor
    ```

