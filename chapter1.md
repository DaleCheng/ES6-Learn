# let和const {#let-const-}

`let`只作用於區塊內

```js
{
    var a = 1;
    var b = 1;
}

console.log(a);    //1
console.log(b);    //b is not defined
```

```js
for (var i = 0; i < 10; i++) {
    i = i + i;
}

console.log(i);    //15

for (let j = 0; j < 10; j++) {
    j = j + j;
}

console.log(j);    //j is not defined
```

由以上兩個範例，可以知道`let`只能在區塊內作用，在區塊外使用會發生錯誤。

另外在`let`宣告變數後，若在宣告之前使用相同的變數名稱則會出錯。

```js
var str = 'hello world';

if (true) {
    str = 'hi world';
    let str  = '';
}
```



