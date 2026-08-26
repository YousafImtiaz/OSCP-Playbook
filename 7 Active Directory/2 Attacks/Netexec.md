> With password (try with and without local auth):

```
netexec <module> <ip_subnet> -u <user> -p '<pass>' <--local-auth> --continue-on-success
```

> With hash:

```
netexec <module> <ip_subnet> -u <user> -H <hash> --local-auth --continue-on-success 
```

> Specify Domain if necessary:

```
netexec <module> <ip_subnet> -u <user> -p <pass> -d <domain> --continue-on-success
```

Protocols that you could try:

```
smb
ssh
ftp
winrm
rdp
mssql
```

