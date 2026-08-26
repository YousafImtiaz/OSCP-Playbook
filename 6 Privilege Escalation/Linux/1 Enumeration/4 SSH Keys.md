If you have an SSH key then try to run it for a different user once you have the list of users on the machine. Also look for .ssh when you run ls -la in users home folders

> Search for keys:

```
find / -name id_rsa 2> /dev/null
find / -name id_ecdsa 2> /dev/null
```
