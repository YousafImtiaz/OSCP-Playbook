> Run in a new terminal window:

```
wpscan --url http://<target_ip> --enumerate p --plugins-detection aggressive
```

> To find usernames:

```
wpscan --url http://<target_ip>/wordpress --enumerate u
```

> To bruteforce password (try rockyou.txt first but this wordlist is an alternative):

```
wpscan --url http://<target_ip>/wordpress -U <username> -P /usr/share/wordlists/metasploit/unix_passwords.txt
```

> We can also target wp-admin (if available) to find usernames and then bruteforce the password:

```
wpscan --url http://<target_ip>/wordpress/ --wp-content-dir wp-admin --passwords /usr/share/wordlists/rockyou.txt 
```
