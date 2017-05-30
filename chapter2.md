# 解構賦值 {#let-const-}

基本用法如下：

```js
let [name1, name2, name3] = ['Dale', 'Jack', 'Bon'];
console.log(name1);    //Dale

let [name1, [name2, name3]] = ['Dale', ['Jack', 'Bon']];
console.log(name2);    //Jack
```

也可以在宣告時，直接給予預設值：

```js
let[name1 = 'Dale', name2] = [, 'Jack'];


let [x, y = 'b'] = ['a']; // x='a', y='b'
let [x, y = 'b'] = ['a', undefined]; // x='a', y='b'
```



