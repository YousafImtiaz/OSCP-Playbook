> Look at listening ports:

```
netstat -tuln
```

If you see a port running such as 443 or 3306 and it was not shown in the nmap scan you can do a port forward using chisel and try to access it on localhost.

> Grep out running processes running as root:

```
ps aux | grep root
```

> View running process in tree format:

```
ps axjf | grep "^ *1 " -A 1000
```

Look for processes here that are running sh scripts specifically.

> If you find nothing consider using pspy to view running processes after transferring it:

```
timeout 2m ./pspy
```

This will show running scripts and you may find credentials here too. 

> You can also use a built in command to grep for specific keywords such as:

```
timeout 30s watch -n 1 "ps -aux | grep pass"
```

Adjust the command to see if you can find certain keywords (grep sudo)

> If you can run tcpdump as sudo try:

```
sudo tcpdump -i lo -A | grep "pass"
```
