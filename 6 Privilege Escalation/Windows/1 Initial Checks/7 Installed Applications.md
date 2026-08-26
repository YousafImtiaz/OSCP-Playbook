> 32 bit applications:

```
Get-ItemProperty "HKLM:\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall\*" | select displayname
```

> 64 bit applications:

```
Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\*" | select displayname
```

> View running applications:

```
Get-Process
```

Search LOLBAS if you find an exe file that looks unusual.