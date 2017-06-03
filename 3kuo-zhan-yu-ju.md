# 擴展語句與Rest參數 {#let-const-}

`rest`參數用於函數的傳入

```js
function testFn(...args) {
    for (var arg of args) {
        console.log(arg);
    }
}

testFn('Dale', 'Ben', 'John');
//Dale
//Ben
//John
```

```js
let numArray = [1, 2, 3, 4, 5];
console.log(numArray);        //[1, 2, 3, 4, 5]
console.log(...numArray);     //1 2 3 4 5
```



