# JavaScript 1

```javascript
// /users?id=123
import express from 'express'
import { db } from './db'
const app = express()

app.get('/users', async (req, res) => {
  const id = req.query.id as string
  if (!id) {
    res.status(400).send('missing id')
  }

  const sql = `SELECT * FROM users WHERE id = ${id}`
  const result = await db.query(sql) 

  res.json(result.rows)
})
```

<details>
<summary>เฉลย</summary>

## เฉลย

- Missing return หลังส่ง 400 → โค้ดอาจส่ง response ซ้ำ / ดำเนินต่อหลัง error.• แก้: if (!id) return res.status(400).send('missing id')

<details>
    <summary>hidden</summary>
    - SQL Injection จากการต่อสตริงด้วย id.• แก้: ใช้ parameterized query เช่น WHERE id = $1, db.query('... where id = $1', [id])
</details>

</details>