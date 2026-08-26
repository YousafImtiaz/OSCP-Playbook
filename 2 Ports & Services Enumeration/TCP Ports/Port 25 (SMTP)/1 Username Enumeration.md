> Go through a list of usernames to see which ones exist:

```
smtp-user-enum -M VRFY -U /usr/share/wordlists/metasploit/unix_users.txt -t <target_ip>
```

> Manual method:

```
nc -nv <target_ip> 25
```

```
telnet <target_ip> 25 
```

