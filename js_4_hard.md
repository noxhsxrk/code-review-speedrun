# JavaScript 4

```javascript
async function getUserDetails(ids) {
  let results = [];
  let user;

  for (let id of ids) {
    user = await fetch(`https://jsonplaceholder.typicode.com/users/${id}`).then(
      (res) => res.json()
    );
    debug.push(user.username);
    if (user.isActive) {
      results.push(user);
    }
  }

  console.log("Debug users:", debug);
  return results;
}

const ids = [1, 2, 3];
getUserDetails(ids).then((users) => {
  console.log("Active users:", users);
});
```

<details>
<summary>เฉลย</summary>

## เฉลย

ไม่มีการ check isActive จริงใน data → logic ผิดที่ assume field มี
วิธีแก้:

```javascript
if (user.username && user.username.length > 0) {
  results.push(user);
}
```

</details>
