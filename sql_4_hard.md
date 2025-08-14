# SQL 4

```sql
SELECT *
FROM products
WHERE id NOT IN (SELECT product_id FROM order_items);
```

<details>
<summary>เฉลย</summary>

# เฉลย

ปัญหา: ถ้า subquery คืน NULL สักค่าเดียว ผลลัพธ์จะเป็นค่าว่างหมด
วิธีแก้: กรอง NULL ออกจาก subquery

WHERE id NOT IN (
  SELECT product_id FROM order_items WHERE product_id IS NOT NULL
);

</details>