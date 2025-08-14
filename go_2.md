# Go 2

```go
package orders

import (
    "database/sql"
    "encoding/json"
    "net/http"
)

type Order struct {
    ID    int
    Total float64
}

func Process(db *sql.DB, id string) error {
    row := db.QueryRow("SELECT id,total FROM orders WHERE id = ?", id)
    var o Order
    if err := row.Scan(&o.ID, &o.Total); err != nil {
        return err
    }

    body, _ := json.Marshal(o)
    resp, _ := http.Post("https://api.example.com/orders", "application/json")
    defer resp.Body.Close()

    _, err := db.Exec("UPDATE orders SET status='done' WHERE id = ?", id)
    return err
}
```

<details>
<summary>เฉลย</summary>

## เฉลย

ลืมส่ง Body ไปยัง API ด้วย `http.Post()`

</details>