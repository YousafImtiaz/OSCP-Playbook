> Wfuzz: (IP Address)

```
wfuzz -c -f sub-fighter -w /usr/share/spiderfoot/spiderfoot/dicts/subdomains-10000.txt -u 'http://<target_ip>' -H "Host:FUZZ.<target_ip>" --hc 400,302
```

> ffuf: (If the website has a name instead of just an IP Address)

```
ffuf -w /usr/share/spiderfoot/spiderfoot/dicts/subdomains-10000.txt -u http://website.com/ -H "Host: FUZZ.website.com"
```
