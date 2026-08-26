> View SPN's in the domain:

```
Get-NetUser -SPN | select samaccountname,serviceprincipalname
```

> Here if we get a URL such as {HTTP/web.domain.com} we can use nslookup to get an IP address and try to access it in the browser:

```
nslookup web.domain.com
```

