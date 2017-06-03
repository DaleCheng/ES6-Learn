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

需注意的是，`resr`參數一定要放在最後面，否則會出錯

```js
function add(arg1, arg2, ...args) {
    let sum = 0;
    for (let num of args) {
        sum += num;
    }
    
    return sum;
}

console.log(add(1, 2, 3, 4, 5));    //
```

```
let numArray = [1, 2, 3, 4, 5];
```

```js
console.log(numArray);        //[1, 2, 3, 4, 5]
console.log(...numArray);     //1 2 3 4 5
```



