# SQL 1

```sql
SELECT *
FROM tasks
WHERE deleted_at = NULL;
```

<details>
<summary>เฉลย</summary>

# เฉลย

`= NULL` จะได้ UNKNOWN เสมอ → ไม่คืนแถวใดๆ

- แก้:

```sql
SELECT *
FROM tasks
WHERE deleted_at IS NULL;
```

</details>
