# Copy SQL Data From One Table to Another Table

```sql
INSERT INTO `database`.`table.new`(`colA`,`colB`,`colC`)
SELECT `colA`,`colB`,`colC`
FROM `database`.`table.old`
```

> This works even between tables with different column structures. Only related columns **must be same**.