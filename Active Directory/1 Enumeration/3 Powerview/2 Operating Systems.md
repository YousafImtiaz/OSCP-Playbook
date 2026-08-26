> Get the full information about computer objects in the domain:

```
Get-NetComputer
```

> Get a clean list of all computers and their associated DNS hostname and OS version

```
Get-NetComputer | select dnshostname,operatingsystem,operatingsystemversion
```
