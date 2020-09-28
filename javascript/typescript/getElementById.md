# `document.getElementById("hoge").value` でエラーが発生する問題
## 起きた問題
HTMLの要素をTypeScriptの`document.getElementById("hoge").value`で取得しようとしました。

そうしたところ、以下のエラーが発生して、要素が取得できませんでした。

```typescript
The property ‘hoge' does not exist on value of type 'HTMLElement'
```

## 解決方法
そもそも、`document.getElementById("hoge")`の戻り値が、HTMLElement型で、その方には`value`プロパティが存在しないということでした。

そのため、`HTMLInputElement`というインターフェースを使うようにすると、`value`プロパティを使うことができます。

```typescript
 const examDate: HTMLInputElement | null = <HTMLInputElement>document.getElementById('examDateCreate');
```

## 知ったところ
[TypeScriptで document\.getElementById\("hoge"\)\.value をすると出るThe property ‘hoge' does not exist on value of type 'HTMLElement' というエラーを解消する \- Qiita](https://qiita.com/Sekky0905/items/a88721f2af41050c93f2)
