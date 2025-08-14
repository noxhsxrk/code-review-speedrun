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

- แท็กผิด (mail) ทำให้ Email ไม่แม็ป• แก้: json:"email"


</details>