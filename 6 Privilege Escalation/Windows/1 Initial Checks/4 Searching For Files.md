**Powershell:**

> Run in users directory:

```
Get-ChildItem -Path C:\xampp -Include *.txt,*.ini -File -Recurse -ErrorAction SilentlyContinue
```

```
Get-ChildItem -Path C:\Users\<username>\ -Include *.txt,*.pdf,*.xls,*.xlsx,*.doc,*.docx -File -Recurse -ErrorAction SilentlyContinue
```

> Run in C:\ drive:

```
Get-ChildItem -Path C:\ -Include *.kdbx -File -Recurse -ErrorAction SilentlyContinue
```

If you see a random exe tool or a sh or ps1 script in a user directory most likely it will be the privesc vector so check permissions on it and try to see what it does.