# 解構賦值 {#let-const-}

基本用法如下：

```js
let [name1, name2, name3] = ['Dale', 'Jack', 'Bon'];
console.log(name1);    //Dale

let [name1, [name2, name3]] = ['Dale', ['Jack', 'Bon']];
console.log(name2);    //Jack

let [name1 = name2, name2 = 'Jack'] = [];
console.log(name1);    //undefined

let {name, age} = {name: 'Dale', age: 29};
console.log(name);     //Dale
console.log(age);      //29
```

也可以在宣告時，直接給予預設值：

```js
let[name1 = 'Dale', name2] = [, 'Jack'];
console.log(name1);    //Dale
console.log(name2);    //Jack

let {name = 'Dale', age = 29} = {};
console.log(name);     //Dale
console.log(age);      //29
```

特別註記-物件的嵌套：

```js
let jsonData = {
    name: 'Dale',
    age: 29,
    hobby: {
        music: 'Jazz',
        sport: 'Basketball'
    }
}

let {name, age, hobby: {music, sport}} = jsonData;

console.log(name);     //Dale
console.log(age);      //29
console.log(music);    //Jazz
console.log(sport);    //Basketball
```



