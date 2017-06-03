# 箭頭函數\(=&gt;\) {#let-const-}

箭頭函數可以讓程式碼可讀性提高，更加簡潔

```js
//Before
function makeWeapon() {
    console.log('get tank...');
}

//After
var weapon = () => {
    console.log('get tank...');
}
```

```js
//Before
function addNumber(...args) {
    let sum = 0;
    for (let num of args) {
        sum += num;
    }

    return sum;
}

//After
var addNumber = (...args) => {
    let sum = 0;
    for (let num of args) {
        sum += num;
    }

    return sum;
}
```

若函式只有一個參數時可以不用寫`()`但是rest參數例外，另外`{}`也可以省略，當省略時也可以不用寫`return`

```js
var sum = 0;

//Before
function counter(num) {
    return sum + num;
}

//After
var counter = num => sum + num;
```

---

箭頭函數在`this`上需特別注意，他會指向定義時所在的對象

```js
function makeWeapon() {
    this.tankNum = 0;
    
    //Before
    setInterval(function() {
        this.tankNum++;
    }, 5000);
    
    //After
    setInterval(() => this.tankNum++, 5000);
}





```



