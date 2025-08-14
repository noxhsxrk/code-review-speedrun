# Go 4

```go
package main

import (
	"fmt"
)

func countLetters(s string) map[rune]int {
	var m map[rune]int
	for _, r := range s {
		m[r] = m[r] + 1
	}
	return m
}

func main() {
	result := countLetters("banana")
	fmt.Println(result)
}
```

<details>
<summary>เฉลย</summary>

## เฉลย (2 จุด)

บรรทัด var m map[rune]int ถูกใช้งานโดยไม่ได้ make ก่อน (เขียนค่าเข้า map nil จะ panic)

```go
func countLetters(s string) map[rune]int {
	m := make(map[rune]int) 
	for _, r := range s {
		m[r] = m[r] + 1
	}
	return m
}
```

</details>
