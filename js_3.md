# JavaScript 3

```javascript
const user = { 
  name: 'Alice', 
  email: 'alice@example.com' 
};

const { name, age } = user;

const greeting = `Hello, ${name}!`;
const userInfo = `Email: ${user.email}, Age: ${age.toUpperCase()}`;
```

<details>
<summary>เฉลย</summary>

## เฉลย
age จะเป็น undefined และการเรียก .toUpperCase() บน undefined จะทำให้เกิด TypeError
วิธีแก้: เพิ่ม default value ให้กับ age หรือตรวจสอบว่าเป็น undefined ก่อนใช้งาน

</details>