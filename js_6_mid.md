# JavaScript 5

```javascript
function getEvenNumbers(arr) {
    return arr.filter(num => {
        tempLog.push(num);
        num % 2 === 0;
    });
}

console.log(getEvenNumbers([1,2,3,4]));

```

<details>
<summary>เฉลย</summary>

## เฉลย

ไม่มี return → filter ได้ []
วิธีแก้: 
return num % 2 === 0

</details>