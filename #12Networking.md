![alt text](Linux.jpg)

# Networking 

In this section we are going to learn about Networking and other networking tools in Linux.


## ```Displaying Routing Table Information```
-   ### ```ip route show```
```
┌──(kali㉿kali)-[~/Desktop]
└─$ ip route show
```

**ip route show** command gives us our routing table details.
**Gateway IP Address**/**router ip address** and our machine's ip address as well.

## ```Displaying Current IP Address```
- ### ```ip addr```
```
┌──(kali㉿kali)-[~/Desktop]
└─$ ip addr
```

**ip addr** shows the **ip address** of the machine in the current session. You can find the address mentioned in the ethernet section, mine is showing in **eth0**.

- ### ```ifconfig```
To display machine ip details we can also use **ifconfig** command. We need the **inet** address.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ ifconfig | grep "inet"
```

## ```netstat```

**netstat** command is used to print Network Connections, routing tables, interface statistic.

### ```DISPLAY ROUTING TABLE```
To display routing table information use the below command.
**netstat -r** command gives us details or information about the routing table.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ netstat -r
```

### ```LISTEN TO OPEN PORTS```
**netstat -l** command is used to listen to open ports which means the device is waiting for connections or listening for incoming traffic applications and processes.
```
┌──(kali㉿kali)-[~]
└─$ netstat -l 
```


## ```netdiscover```

**netdiscover** command is used to scan the network and display current number of hosts present in the network. You need to have **sudo privileges** to execute the command and also mention the interface you are checking.

```
┌──(kali㉿kali)-[~]
└─$ sudo netdiscover -i eth0
```

### ***/etc/resolv.conf***
The /etc/resolv.conf file in Linux is used to configure how the system uses the Domain Name System (DNS) to resolve host names and IP addresse


### ***/etc/hosts***
The /etc/hosts file in Linux is a plain text file that maps hostnames to IP addresses