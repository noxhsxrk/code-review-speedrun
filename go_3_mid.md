# Go 3

```go
package main

import "fmt"

type User struct {
  Name string
}

func getUserName(user *User) string {
  return user.Name
}

func main() {
  var user *User
  fmt.Println(getUserName(user))
}
```

<details>
<summary>เฉลย</summary>

## เฉลย

- ปัญหา: user เป็น nil ทำให้เกิด panic เมื่อพยายามเข้าถึง user.Name
- วิธีแก้: ตรวจสอบ user ว่าเป็น nil ก่อนใช้งาน

```go
if user == nil {
  return ""
}

```

</details>
