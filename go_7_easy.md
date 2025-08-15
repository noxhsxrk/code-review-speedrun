# Go 7

```go
package main

import (
    "fmt"
    "os"
)

func main() {
    err := os.WriteFile("data.txt", []byte("hello"), 0644)
    if err == nil {
        fmt.Println("Error writing file:", err)
    }
}

```

<details>
<summary>เฉลย</summary>

## เฉลย

- ปัญหา: เช็ค error กลับด้าน ทำให้ไม่รู้ว่ามี error จริง
- วิธีแก้: `if err != nil { ... }`

</details>
