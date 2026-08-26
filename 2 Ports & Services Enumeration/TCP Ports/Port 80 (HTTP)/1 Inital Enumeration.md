> Find interesting directories:

```
sudo nmap -p 80 --script http-enum <target ip>
```

> Pull the website header:

```
curl -I <target_ip>
```

> Enter the IP address in the browser. If it leads to a website with a name then add it to /etc/hosts:

```
<target_ip> <domain_name> 
```


> Quick checks after finding a website:

- Check the Apache server version for an exploit on Google.
 
- Check Wappalyzer to see what is running and check the version numbers on Google for exploits.
 
- Check the source code on the landing page or any directory you discover to find a version number or any other interesting data that may stand out. Use CTRL + F to search for keywords like password, hidden, or username.

- Search the website title on Searchsploit, as well as anything else on the website that looks related to software of some kind. You might be able to find something.

- Google the framework the site is running with the word "exploit." Even if you don't have the version the exploit may work anyway especially if its on the first page.

- If browsing to port 80 is just a default page, run Gobuster right away.