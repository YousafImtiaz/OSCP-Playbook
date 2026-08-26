> Login:

```
mssqlclient.py <user>:<pass>@<target_ip> -windows-auth
```

> Show version:

```
SELECT @@version;
```

> Show all databases:

```
SELECT name FROM sys.databases;
```

> View tables in a database:

```
SELECT * FROM <table name>.information_schema.tables;
```

> View entries in a table:

```
select * from <catalog>.<schema>.<name>;
```

