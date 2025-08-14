# Go 6

```go
package main

import "fmt"

func main() {
    src := []int{1, 2, 3}
    dst := make([]int, 0)
    copy(dst, src)
    fmt.Println(dst)
}
```

<details>
<summary>เฉลย</summary>

## เฉลย

ปัญหา: slice ปลายทางต้องมีความยาวเพียงพอ
วิธีแก้: dst := make([]int, len(src))

</details>
