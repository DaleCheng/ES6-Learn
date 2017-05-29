# 解構賦值 {#let-const-}

基本用法如下：

```js
let [name1, name2, name3] = ['Dale', 'Jack', 'Bon'];
console.log(name1);    //Dale

let [name1, [name2, name3]] = ['Dale', ['Jack', 'Bon']];
console.log(name2);    //Jack
```



