> Find local admin access on computers under the current user:

```
Find-LocalAdminAccess
```

> If we find a client with admin access we can inspect the machine further:

```
Get-NetSession -ComputerName <admin_computer_name>
```

> Check what user is logged into the computer (usually requires higher privileges):

```
Get-NetSession -ComputerName <computer_name> -Verbose
```

> If we cant see which user is logged on we could use a tool called PsLoggedon.exe:

```
.\PsLoggedon.exe \\<computer_name>
```
