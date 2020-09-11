# Bootstrapのデフォルト値を変更する
## Bootstrapでh1のfont-sizeのデフォルトを変更したい場合
以下のように書くことでBootstrapデフォルト値を変更することができます。

```css
// appliction.scss

$h1-font-size: 2rem

@import "bootstrap";
```

用意されているデフォルトの変数は以下にあります。

[bootstrap\-sass/\_variables\.scss at master · twbs/bootstrap\-sass · GitHub](https://github.com/twbs/bootstrap-sass/blob/master/assets/stylesheets/bootstrap/_variables.scss)

1点注意すべきこととして、変数の上書きの後に`import`する必要があります。  
これを逆にしてしまうと変数が上書きされません。

## 学んだところ
- 社内研修
- [Bootstrap テーマ \- Bootstrap 4\.2 \- 日本語リファレンス](https://getbootstrap.jp/docs/4.2/getting-started/theming/) 
