> Look for a kdbx file using PS:

```
Get-ChildItem -Path C:\ -Include *.kdbx -File -Recurse -ErrorAction SilentlyContinue
```

If we find a file we need to transfer it to our Kali machine using smbserver and then crack it.