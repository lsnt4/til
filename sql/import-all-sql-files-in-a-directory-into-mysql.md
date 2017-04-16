# Import All SQL Files In A Directory Into MySQL

```sql
for SQL in *.sql; do DB=${SQL/\.sql/}; echo Importing $DB; mysql -u root -pMySuperSecretPassword $DB < $SQL; done
```

Source: [StackOverflow](http://stackoverflow.com/a/12481305/3683435)