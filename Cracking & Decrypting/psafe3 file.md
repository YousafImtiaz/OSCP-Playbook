> Convert it to a hash then crack with john:

```
pwsafe2john <file> > hash.txt
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt 
```

> To view the file after cracking the password:

```
pwsafe <filename> 
```
