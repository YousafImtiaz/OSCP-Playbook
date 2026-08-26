TCP & UDP scans:

I used my tool here: https://github.com/YousafImtiaz/Nportsc/tree/main

```
sudo python3 /home/kali/nportsc.py <ip> --tcp T4
```

```
sudo python3 /home/kali/nportsc.py <ip> --udp T4
```

REVERT IF SCAN TAKES LONGER THAN 5 MINUTES. You can also use the -Pn flag if it says the host is down.

> Manual Method: TCP Ports

```
sudo nmap -p- -T4 <IP>
```

```
sudo nmap -p <ports> <IP> -sC -sV
```

> Manual Method: UDP Ports

```
sudo nmap -sU --top-ports=100 --open -T4 <IP>
```

```
sudo nmap -sU -p <ports> -sV <IP>
```


> Tips:

Scan a port individually if you see a tcpwrapped message in case it may reveal information:

```
sudo nmap -p <port> <IP>
```

> If the scan is taking too long even after a revert then run:

```
sudo nmap -p- -T4 <IP> -Pn -vvv
```

> If you're still having issues then you should try to lower the MTU:

```
sudo ifconfig tun0 mtu 1250
```

