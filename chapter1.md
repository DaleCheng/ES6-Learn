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

---

另外在`let`宣告變數後，若在宣告之前使用相同的變數名稱則會出錯，這是因為暫時性的死區temporal dead zone\(TDZ\)關係。

```js
var str = 'hello world';    //ReferenceError: str is not defined

if (true) {
    str = 'hi world';       //ReferenceError: str is not defined

    let str;
    console.log(str);       //undefined

    str = 'hi world';
    console.log(str);       //hi world

}
```

`let`也不能重複宣告同一個變數，在同一個區塊內。函數內也不能重新宣告相同的變數。

```js
function func() {
    let str = 'Dale';
    var str = 'Jack';        //SyntaxError: Identifier 'str' has already been declared
}

function func(str) {         //SyntaxError: Identifier 'str' has already been declared
    let str = 'Dale';
}
```

---

`const`通常用在宣告一個常量值，一旦宣告後就不可改變

```js
const PI = 3.1415;
console.log(PI);            //3.1415

PI = 0;                     //TypeError: Assignment to constant variable.
```

另外經`const`宣告的參數要馬上初始化，賦予值，否則將會直接出錯

```js
const PI;                  //SyntaxError: Missing initializer in const declaration
```



