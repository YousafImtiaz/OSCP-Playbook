> Standard login:

```
ssh <username>@<target_ip>
```

> If SSH is running on a non standard port:

```
ssh <username>@<target_ip> -p <port>
```

> If we get host key verification failed:

```
ssh -i id_rsa -p 2222 dave@192.168.191.201 -o StrictHostKeyChecking=no 
```

