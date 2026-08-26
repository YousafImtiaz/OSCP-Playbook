> Accessing MySQL from localhost after a port forward if mysql is running as root:

```
mysql -u root -h 127.0.0.1 -P 3306 --skip-ssl
```

> Basic navigation commands:

```
show databases;
use <database>;
show tables;
describe <tablename>;
```

> Once we are in a table where we want to extract information:

```
select * from <table_name>;
```
