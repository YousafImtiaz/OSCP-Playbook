> Manual directory checks:

`/robots.txt`
`/admin`
`/login.php`
`/sitemap.xml`

> Find common directories (smaller wordlist):

```
gobuster dir -u http://<ip>/ -w /usr/share/wordlists/dirb/common.txt -x pdf,text,html,php -t 5
```

> Search through more directories (This takes longer so run it in the background while looking through the results of common.txt):

```
ffuf -u http://<target_ip>/FUZZ -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -fc 403,302 
```

If you find a directory listing or any other page that doesn't look like a dead end, search recursively, especially for something such as /api.

If you see a license directory when directory busting, it's not custom software but licensed, which means it will most likely have a CVE.

Another wordlist you may want to try:

```
/usr/share/wordlists/dirb/big.txt
```
