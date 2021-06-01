# Find largest record

## Find third largest record from a table using LIMIT

Query to find third largest salary record from employee table

```sql
SELECT * 
FROM employee_info
ORDER BY salary
LIMIT 2, 1 
```
