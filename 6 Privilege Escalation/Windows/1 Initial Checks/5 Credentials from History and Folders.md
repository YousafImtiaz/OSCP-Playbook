> View terminal history in Powershell:

```
history
```

> Also look the environmental variables in powershell to see if there may be a password there:

```
dir env:
```

> In CMD you can check for stored credentials using:

```
cmdkey /list
```

> You can also query the registry to try and find some credentials:

```
reg query HKLM /f password /t REG_SZ /s
```

> Places to look for interesting files (If you are in RDP, enable hidden files in File Explorer as well):

```
- Documents and Download folders of any users you have access to
- C:\ Drive (look for SAM and SYSTEM files)
- C:\Program Files
- AppData directory
- C:\TEMP
- C:\ProgramData\ApplicationName\Logs
```

> Wherever you find unusual or non standard files download or view them and search for keywords like:

```
password
NTLM
username
administrator
```

> Once you find an interesting file such as an exe file run:

```
icacls <filename>
```

This will show you the permissions you have over it.