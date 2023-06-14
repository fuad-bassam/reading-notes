# SQL

## pagination

---

```SQL
 SELECT * FROM (SELECT ROW_NUMBER() OVER(ORDER BY Docn_link DESC) AS NUMBER, * FROM DOC00175 WHERE DOCN_DEL = 0
AND (FOLD_VAL = '_Default' or  FOLD_VAL = '' OR FOLD_VAL = '10')
AND DOCN_LVL <= 99) AS TBL WHERE NUMBER BETWEEN ((1 - 1) * 20 + 1) AND (1 * 20) ORDER BY Docn_link DESC
```

---

## check changes in script

---

```SQL
 SELECT type, name as 'Stored Procedure Name',CONVERT(varchar, modify_date, 100) as 'Modify Date'
FROM sys.objects
WHERE 
YEAR(modify_date)= Year(GETDATE())
--and type in ('P','TR','V')
order by modify_date desc
```

---
