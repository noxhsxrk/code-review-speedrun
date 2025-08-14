# JavaScript 5

```javascript
async function fetchData() {
    console.log("Fetching...");
    const data = fetch('https://poramest-vichitnoppatwo/sod/1');
    console.log(await data.json());
}

fetchData();
```

<details>
<summary>เฉลย</summary>

## เฉลย

ลืม await ก่อน fetch
วิธีแก้: 
const res = await fetch(...);
console.log(await res.json());

</details>