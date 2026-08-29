> After getting the id_rsa file, run chmod to prevent "permissions too open" error:

```
chmod 600 id_rsa
```

> Now we convert the key to a hash then crack the passphrase with john:

```
ssh2john id_rsa > id_rsa.hash 
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt id_rsa.hash 
```
