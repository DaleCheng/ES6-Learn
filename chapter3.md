# 擴展運算符與Rest參數 {#let-const-}

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
function addNumber(arg1, arg2, ...args) {
    let sum = 0;
    for (let num of args) {
        sum += num;
    }

    return sum;
}

console.log(addNumber(1, 2, 3, 4, 5));    //12
```

```js
//SyntaxError
function addNumber(arg1, ...args, arg2) {
    let sum = 0;
    for (let num of args) {
        sum += num;
    }

    return sum;
}
```

擴展運算符像是rest參數的逆運算，可以把陣列轉乘列表，也可以合併陣列

```js
console.log(...[1, 2, 3]);    //1 2 3

let numArray1 = [1, 2, 3];
let numArray2 = [4, 5, 6];
console.log([...numArray1, ...numArray2]);    //[1, 2, 3, 4, 5, 6]
```

組合運用

```js
let numArray = [1, 2, 3, 4, 5];

function add(...args) {        //rest參數
    let sum = 0;
    for (let num of args) {
        sum += num;
    }

    return sum;
}

console.log(add(...numArray)); //擴展運算符
```

與解構賦值搭配

```
let [first, ...rest] = [1, 2, 3, 4, 5];
first //1
rest  //[2, 3, 4, 5]
```



