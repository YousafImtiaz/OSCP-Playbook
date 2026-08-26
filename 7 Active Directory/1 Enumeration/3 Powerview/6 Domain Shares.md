> Find shares in the domain: (use the -CheckShareAccess flag to show shares only available to us):

```
Find-DomainShare <-CheckShareAccess>
```

> If we find a share we want to view we can enumerate it further by viewing its path:

```
ls \\<computer name>\<sharename>\<domain name>\
```
