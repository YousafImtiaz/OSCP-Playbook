> General command (use this as a baseline and then modify flags based on what works):

```
sudo hashcat -m <module> -a 0 <path_to_hashfile> /usr/share/wordlists/rockyou.txt --force
```
