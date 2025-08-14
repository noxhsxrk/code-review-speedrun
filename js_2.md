# JavaScript 2

```javascript
// ตั้งคุกกี้อายุ 1 ชั่วโมง
app.get('/login', (req, res) => {
  const sid = 'abc123'
  res.cookie('sid', sid, { expires: new Date(Date.now + 60 * 60 * 1000) })
  res.send('ok')
})
```

<details>
<summary>เฉลย</summary>

## เฉลย

- ใช้ Date.now แทน Date.now() → ได้ Invalid Date • แก้: new Date(Date.now() + 60 * 60 * 1000)

</details>