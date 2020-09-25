# TypeScriptとは
## JavaScriptとどのように異なるのか
- JavaScriptのスーパーセット。
- JavaScriptに型を導入したもの。
- 型の導入によりコンパイル時にエラーが検知できるようになった。

## コードのスタイル規約
スタイル規約は`tslint.json`に持たせます。  
以下のように設定することができます。
```json
{
  "defaultSeverity": "error",
     "extends": [
        "tslint:recommended"
     ],
    "rules": {
      "semicolon": false,
      "trailing-comma": false
    }
}
```
> Boris Cherny 『プログラミングTypeScript』p13-14 より

## 学んだところ
- [TypeScript: Typed JavaScript at Any Scale.](https://www.typescriptlang.org/)
- [TypeScript の概要 - Qiita](https://qiita.com/EBIHARA_kenji/items/4de2a1ee6e2a541246f6)
- [TypeScript - Wikipedia](https://ja.wikipedia.org/wiki/TypeScript)
- [TypeScript vs CoffeeScript: Which One To Choose For Writing Better JS](https://analyticsindiamag.com/typescript-vs-coffeescript-which-one-to-choose-for-writing-better-javascript/)

