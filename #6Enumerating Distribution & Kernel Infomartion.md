![alt text](Linux.jpg)

# Enumerating Distribution and Kernel Information in Linux

In this section we are going to learn to enumerate distribution and gather kernel information in Linux.

## ```whoami```

**whomai** command is used to display the current username.
```
┌──(kali㉿kali)-[~]
└─$ whoami
kali
```

## ```hostname```

**hostname** show or set the system's host name.
```
┌──(kali㉿kali)-[~]
└─$ hostname
kali
```

## ```id```

**id** command shows the current user id. A user ID (UID) in Linux is a unique numerical identifier that identifies a user account in the Linux system.

```
┌──(kali㉿kali)-[~]
└─$ id
uid=1000(kali) gid=1000(kali) groups=1000(kali),4(adm),20(dialout),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),100(users),101(netdev),106(bluetooth),113(scanner),136(wireshark),137(kaboxer)
```

## ```groups```

**groups** command is used to display the list of groups the current user is connected to. Groups are nothing but a collection of users.

```
┌──(kali㉿kali)-[~]
└─$ groups kali
kali : kali adm dialout cdrom floppy sudo audio dip video plugdev users netdev bluetooth scanner wireshark kaboxer

┌──(kali㉿kali)-[~]
└─$ groups root
root : root
```

## ```lsb```

**lsb** command is used to display information of the system.
```
┌──(kali㉿kali)-[~]
└─$ lsb_release -a
No LSB modules are available.
Distributor ID: Kali
Description:    Kali GNU/Linux Rolling
Release:        2024.3
Codename:       kali-rolling
```

## ```lscpu```

**lscpu** command to enumerate information about processor and cpu.

```
┌──(kali㉿kali)-[~]
└─$ lscpu
Architecture:             x86_64
  CPU op-mode(s):         32-bit, 64-bit
  Address sizes:          40 bits physical, 48 bits virtual
  Byte Order:             Little Endian
CPU(s):                   4
  On-line CPU(s) list:    0-3
Vendor ID:                AuthenticAMD
  Model name:             AMD Ryzen 7 4800H with Radeon Graphics
    CPU family:           23
    Model:                96
    Thread(s) per core:   1
    Core(s) per socket:   2
    Socket(s):            2
    Stepping:             1
    BogoMIPS:             5789.14
    Flags:                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov 
                          pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext rdtsc
                          p lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid
                           extd_apicid tsc_known_freq pni pclmulqdq ssse3 fma cx16 sse4_
                          1 sse4_2 movbe popcnt aes xsave avx hypervisor lahf_lm abm sse
                          4a misalignsse 3dnowprefetch osvw ssbd vmmcall arat overflow_r
                          ecov succor
Virtualization features:  
  Hypervisor vendor:      VMware
  Virtualization type:    full
Caches (sum of all):      
  L1d:                    128 KiB (4 instances)
  L1i:                    128 KiB (4 instances)
  L2:                     2 MiB (4 instances)
  L3:                     32 MiB (4 instances)
NUMA:                     
  NUMA node(s):           1
  NUMA node0 CPU(s):      0-3
Vulnerabilities:          
  Gather data sampling:   Not affected
  Itlb multihit:          Not affected
  L1tf:                   Not affected
  Mds:                    Not affected
  Meltdown:               Not affected
  Mmio stale data:        Not affected
  Reg file data sampling: Not affected
  Retbleed:               Mitigation; untrained return thunk; SMT disabled
  Spec rstack overflow:   Vulnerable: Safe RET, no microcode
  Spec store bypass:      Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer saniti
                          zation
  Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIB
                          RS Not affected; BHI Not affected
  Srbds:                  Not affected
  Tsx async abort:        Not affected
```

## ```uname```

**uname** command used to print system and kernel information.
You can use the **uname** with **-a** switch to display all kernel and version related details.
```
┌──(kali㉿kali)-[~]
└─$ uname -a
Linux kali 6.8.11-amd64 #1 SMP PREEMPT_DYNAMIC Kali 6.8.11-1kali2 (2024-05-30) x86_64 GNU/Linux
```