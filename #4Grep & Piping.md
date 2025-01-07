![alt text](Linux.jpg)

# Grep and Piping using Linux

In this section we are going to learn about grep utility and piping in Linux.

# ```grep```

**grep** command is mainly used we want to filter our search for a particular or specific data/content within a file. **Grep** helps us find strings or pattersn in files.

Let's say I want to search for the word "**Arguments**" in the file **util.asm**. After running the below command we can see all the matches for the word "**Arguments**" have been printed. Using **grep** as shown below we should be aware that the keyword for the search will be case sensitive.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ grep "Arguments" util.asm 
; Arguments:
; Arguments:
; Arguments:
; Arguments:
```

To ommit case sensitive searches we can use the **-i** switch within **grep** command as shown below.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ grep -i "Arguments" util.asm
; Arguments:
; Arguments:
; Arguments:
; Arguments:
; arguments:
```

## ```Piping```

We learnt one way to use **grep** which was the most basic method. We can also use the **Piping** method along with **grep** to get our results. In **Piping** we use **|**  symbol.

I first used **cat** command to print the contents of util.asm file and then **piped** the output where I used the **grep** command to look for the string "**Arguments**" ommiting case sensitivity. In **piping** we are passing output of one command (***cat***) and processing it with another command(***grep***).
```
┌──(kali㉿kali)-[~/Desktop]
└─$ cat util.asm | grep -i "Arguments"
; Arguments:
; Arguments:
; Arguments:
; Arguments:
; arguments:
```