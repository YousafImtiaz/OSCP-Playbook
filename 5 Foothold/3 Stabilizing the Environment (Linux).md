After getting a shell sometimes we will need to stabilize it so it acts like a normal terminal.

> This one works most of the time:

```
python3 -c 'import pty;pty.spawn("/bin/bash")'
```

> Others you could try:

```
python -c 'import pty; pty.spawn("/bin/bash")'
```

```
/usr/bin/python3 -c 'import pty;pty.spawn("/bin/bash")'
```
