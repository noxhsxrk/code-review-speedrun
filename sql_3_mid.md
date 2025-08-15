# SQL 3

```sql
SELECT *
FROM invoices
WHERE issue_date BETWEEN '2025-08-01' AND '2025-08-31';
```

<details>
<summary>เฉลย</summary>

# เฉลย

ปัญหา: ถ้า issue_date เป็น datetime ข้อมูลวันที่ 31 หลังเวลา 00:00 จะไม่ถูกเลือก
วิธีแก้:

```sql
WHERE issue_date >= '2025-08-01'
  AND issue_date < '2025-09-01';
```

</details>
