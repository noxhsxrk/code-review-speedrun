# Go 1

```go
package parse

import (
  "encoding/json"
  "io"
)

type User struct {
  Name  string
  Email string `json:"mail"`
}

func Parse(r io.Reader) (User, error) {
  var u User
  if err := json.NewDecoder(r).Decode(&u); err != nil {
    return User{}, err
    }
  return u, nil
}
```

<details>
<summary>เฉลย</summary>

## เฉลย

- ปัญหา: tag json:"mail" ทำให้ Email ไม่แมปจาก JSON จริง
- วิธีแก้: เปลี่ยนเป็น json:"email"

```go
type User struct {
  Name  string
  Email string `json:"email"`
}

```

</details>
