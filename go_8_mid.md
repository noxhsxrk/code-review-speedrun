# Go 8

```go
// scanBug.go
// 1. โปรแกรมต้อนรับผู้ใช้
// 2. ขอให้ผู้ใช้กรอกชื่อ
// 3. อ่านข้อมูลจาก stdin
// 4. แสดงข้อความต้อนรับ
// (แต่มีบางอย่างผิดปกติ)

package main

import (
    "fmt"
    "strings"
    "time"
)

func main() {
    fmt.Println("Welcome to our program!")
    fmt.Println("Please enter your name:")

    var name string

    time.Sleep(500 * time.Millisecond)
    fmt.Println("Processing...")

    fmt.Scan(name)

    upperName := strings.ToUpper(name)

    fmt.Printf("Hello, %s! We're glad to see you.\n", upperName)
}

```

<details>
<summary>เฉลย</summary>

## เฉลย

ปัญหา: fmt.Scan(name) ต้องใช้ pointer (&name) เพื่อให้ฟังก์ชันเขียนค่าลงตัวแปร
วิธีแก้:

fmt.Scan(&name)

</details>
