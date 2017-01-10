# Copy SQL Data From One Table to Another Table

```sql
INSERT INTO `database`.`table_new`(`colA`,`colB`,`colC`)
SELECT `colA`,`colB`,`colC`
FROM `database`.`table_old`
```

> This works even between tables with different column structures. Only related columns **must be same**.

## Another example with more tables

INSERT INTO `table_new`(`colA`,`colB`,`colC`,`colD`)
SELECT `colA`,`colB`,`colC`,`colD` FROM `table_old_1`
UNION ALL
SELECT `colA`,`colB`,`colC`,`colD` FROM `table_old_2`
UNION ALL
SELECT `colA`,`colB`,`colC`,`colD` FROM `table_old_3`;