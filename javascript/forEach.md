# JavaScriptの`forEach`の落とし穴
## Array.prototype.forEach()
`Array.prototype.forEach()`は、`empty`をスキップする。  
以下のように、配列を定義すると配列を`empty`という要素が作成される。

この時、`empty`を含む配列`array1`に対して`forEach`をすると、`empty`はスキップされて、2回しかループが回らない…。

```javascript
let array1 = ['a', ,'c'];

console.log(array1);
arrya1.forEach(element => console.log(element));

//=> ["a", empty, "c"]
//=> "a"
//=> "c"
```
## `empty`を含む配列の`length`は…
以下のように`empty`を含んだ要素数になる…。
```javascript
let array1 = ['a', ,'c'];
console.log(array1.length);

//=> 3
```
## 補足
- 2020.08.31の[Sendagaya\.rb \#327](https://sendagayarb.doorkeeper.jp/events/110912) で上記を知りました。
- [Array\.prototype\.forEach\(\) \- JavaScript \| MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

