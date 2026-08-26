> Basic information about the domain:

```
Get-NetDomain
```

> List all users in the domain with detail:

```
Get-NetUser
```

> See usernames only: 

```
Get-NetUser | select cn
```

> See all groups:

```
Get-NetGroup | select cn
```

> Enumerate a specific group and see "nested" groups:

```
Get-NetGroup "<group_name>" | select member

Get-NetGroup -GroupName *admin*
```
