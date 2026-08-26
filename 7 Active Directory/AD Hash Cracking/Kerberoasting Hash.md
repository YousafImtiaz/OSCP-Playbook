> After performing a Kerberoasting attack:

```
sudo hashcat -m 13100 -a 0 <path_to_hashfile> /usr/share/wordlists/rockyou.txt --force
```
