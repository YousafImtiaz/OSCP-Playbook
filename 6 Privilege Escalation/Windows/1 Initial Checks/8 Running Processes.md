> Look at listening ports:

```
netstat -an | find "LISTENING"
```

If you see a port running such as 443 or 3306 and it was not shown in the nmap scan you can do a port forward using chisel and try to access it.
