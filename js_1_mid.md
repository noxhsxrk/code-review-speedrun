# JavaScript 1
```javascript

async function validateUser(user) {
  console.log('Validating user:', user.name)
  if (!user.email.includes('@')) {
    console.error('❌ Invalid email')
  }
  console.log('Validation passed')
}

async function saveUser(user) {
  console.log('Saving user to DB...')
  await new Promise(r => setTimeout(r, 200))
  console.log('✅ Saved:', user.name)
}

async function main() {
  const user = { name: 'Bob', email: 'bob-at-example.com' }
  await validateUser(user)
  await saveUser(user)
}

main()

```

<details>
<summary>เฉลย</summary>

## เฉลย

ข้อผิดพลาด: ไม่มี return หลัง validation fail ทำให้ saveUser ทำงานต่อ
if (!user.email.includes('@')) return console.error('❌ Invalid email')


</details>