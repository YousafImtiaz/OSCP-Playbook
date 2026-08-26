```
id
```

```
whoami 
```

```
hostname
```

```
ip addr
```

View files with `cat` or use `head` to only see the beginning of it instead of the entire file. If its a config file then use `strings` to extract hardcoded information that the `cat` command cant read or output.

Make sure to check permissions of directories and files using `ls -la` in case you may be in the group which has privileges over it.
