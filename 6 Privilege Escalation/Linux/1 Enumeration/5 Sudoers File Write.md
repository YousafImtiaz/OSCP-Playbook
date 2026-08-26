```
ls -la /etc/sudoers
```

> If you have write access then you can add your own line:

```
nano /etc/sudoers

<your_username> ALL=(ALL:ALL) ALL
```

> If nano is not available then use echo: 

```
'echo <username> ALL=(ALL:ALL) ALL' >> /etc/sudoers
```
