# Find largest record

## Find third largest record from a table using LIMIT

Query to find third largest salary record from employee table

```sql
SELECT * 
FROM employee_info
ORDER BY salary
LIMIT 2, 1 
```

## Find N'th largest record without using LIMIT

```sql
SELECT * 
FROM employee_info e1
WHERE N-1 = 
   (
      SELECT COUNT(DISTINCT salary)
      FROM employee_info e2
      WHERE e1.salary < e2.salary
    )
```
