> List shares available (Press enter when asked for a password):

```
smbclient -L \\\\<target ip>\\
```

> To view a share: (if you have anonymous access)

```
smbclient \\\\<target ip>\\<share name>
```

> To view a share with credentials:

```
smbclient -L \\\\<target_ip>\\ -U <domain>/<username> --password='<password>'
```

```
smbmap -H $IP -u <username> -d <domain>
```


> Try a null session if you dont have anonymous access:

```
smbclient -L <target-ip> -U "" -N
```

```
smbclient -L \\\<target_ip> -U ''
```
