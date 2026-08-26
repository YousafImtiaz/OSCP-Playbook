An object in AD may have a set of permissions applied to it with multiple Access Control Entities. (ACE). These ACEs make up the the Access Control List (ACL). Each ACE defines whether access to the specific object is allowed or denied.

> View Access Control Entities:

```
Get-ObjectAcl -Identity <username>
```

> Here it will output some information including SID's which we can convert to understand what it means:

```
Convert-SidToName <SID>
```

The highest access permission we can have on an object is GenericAll. We can use the following command to display values that equal Generic All and then show only the SID:

```
Get-ObjectAcl -Identity "<group_name>" | ? {$_.ActiveDirectoryRights -eq "GenericAll"} | select SecurityIdentifier,ActiveDirectoryRights
```

> Now we can convert the SID's into names:

```
"<sid>","<sid>" | Convert-SidToName
```
