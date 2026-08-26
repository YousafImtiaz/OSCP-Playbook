> View NFS shares from a target server:

```
showmount -e <target_ip>
```

> If you get a result (e.g. /backup), then we can mount this folder to our machine so we can view it:

```
sudo mkdir mountenum
sudo mount -t nfs <target_ip>:/backup mountenum/
```

Now we can go into the backups folder and we should have a bunch of files to enumerate through.