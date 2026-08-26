> Once the agent is connected now we can run autoroute to do everything automatically or:

```
session > 1
ifconfig
```

Here take note of the the IP address (e.g. 172.16.177.236/24)

> Now we need to add that to our route on kali:

```
sudo ip route add 172.16.x.0/24 dev ligolo
```

> Verify it was added:

```
ip route
```

> Now on ligolo-ng we run:

```
start
```
 