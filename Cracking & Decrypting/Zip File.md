> John:

```
zip2john <file> > ziphash.txt
```

```
john --wordlist=/usr/share/wordlists/rockyou.txt ziphash.txt 
```


>Fcrackzip:

```
fcrackzip -v -u -D -p /usr/share/wordlists/rockyou.txt <filename>
```

