### テーブルサイズを見積もる
```sql
SELECT
    table_name AS `Table`,
    round(((data_length + index_length) / 1024 / 1024), 2) `Size in MB`
FROM information_schema.TABLES
WHERE table_schema = "schema_name" AND table_name = 'table_name'
ORDER BY `Size in MB` DESC
```

### 権限を振る
```sql
GRANT ALL PRIVILEGES ON *.* TO root@'ipaddress' IDENTIFIED BY 'password' WITH GRANT OPTION;
```
ipaddressは%をワイルドカードとして扱える 192.168.%など
