> Always run ls -la to see hidden files, also check:

```
history
```
 
```
cat .bash_history 
```

```
cat .bashrc
```

```
env
```

> Run in the home folder:

```
find . -type f -exec grep -i -I --color=always "PASSWORD" {} /dev/null \;
```

> Directories to check for interesting files:

```
/opt
/tmp
/var/www/html
/var/tmp
/dev/shm
```
