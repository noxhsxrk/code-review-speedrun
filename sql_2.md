# SQL 2

```sql
SELECT *
FROM products
WHERE price > '100'
AND in_stock = true
ORDER BY created_at;
```

<details>
<summary>เฉลย</summary>

# เฉลย

ข้อผิดพลาด: การเปรียบเทียบตัวเลขเป็น string อาจทำให้การจัดเรียงผิดและไม่ใช้ indexวิธีแก้: ใช้ตัวเลขตรง ๆ เช่น WHERE price > 100

</details>