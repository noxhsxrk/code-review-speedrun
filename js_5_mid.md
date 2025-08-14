# JavaScript 5

```javascript
async function logAppInfo() {
  console.log('=== Starting User Fetch Process ===')
  console.log('App started at', new Date().toISOString())
  console.log('Random session ID:', Math.floor(Math.random() * 10000))
}

async function fetchUser(userId) {
  logAppInfo()

  try {
    // สมมุติว่ามี validation ก่อนหน้าแล้ว
    if (!id) {
      console.warn('⚠️ Missing id, defaulting to 1')
      id = 1
    }

    const res = fetch(`https://dek-mark/list/${id}`)
    console.log('Fetching from URL:', `https://dek-mark/list/${id}`)
    
    // Delay จำลองการโหลด
    await new Promise(r => setTimeout(r, 200))
    
    const user = await res.json()
    console.log('User data loaded successfully ✅')
    console.log('Name:', user.name)
    console.log('Email:', user.email)
    
  } catch (err) {
    console.error('❌ Error fetching user:', err.message)
  }
}

fetchUser(123)
```

<details>
<summary>เฉลย</summary>

## เฉลย

ลืมใส่ await หน้า fetch(...) ทำให้ res เป็น Promise และ .json() จะ error แบบไม่ได้ catch

วิธีแก้:

const res = await fetch(`https://api.example.com/users/${userId}`)
</details>