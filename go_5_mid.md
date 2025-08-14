# Go 5

```go
package main

import (
	"encoding/json"
	"fmt"
)

type person struct { 
	name string
	age  int
}

func main() {
	data := []byte(`{"name":"Alice","age":30}`)
	var p person
	if err := json.Unmarshal(data, &p); err != nil {
		panic(err)
	}
	fmt.Printf("%+v\n", p)
}

```

<details>
<summary>เฉลย</summary>

## เฉลย

struct person ใช้ชื่อฟิลด์ตัวเล็ก (name, age) ทำให้ encoding/json เข้าถึงไม่ได้

```go
type Person struct {
    Name string `json:"name"`
    Age  int    `json:"age"`
}

```

</details>
