> SNMP MIB values used with snmpwalk for enumeration:

| 1.3.6.1.2.1.25.1.6.0   | System Processes |
| ---------------------- | ---------------- |
| 1.3.6.1.2.1.25.4.2.1.2 | Running Programs |
| 1.3.6.1.2.1.25.4.2.1.4 | Processes Path   |
| 1.3.6.1.2.1.25.2.3.1.4 | Storage Units    |
| 1.3.6.1.2.1.25.6.3.1.2 | Software Name    |
| 1.3.6.1.4.1.77.1.2.25  | User Accounts    |
| 1.3.6.1.2.1.6.13.1.3   | TCP Local Ports  |

```
snmpwalk -c public -v1 <target_ip> <mib value>
```

> Retrieve entire output:

```
snmpwalk -v1 -c public <target_ip> NET-SNMP-EXTEND-MIB::nsExtendObjects
```


