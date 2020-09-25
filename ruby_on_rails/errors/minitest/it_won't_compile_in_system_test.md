# システムテストで JavaScript 関連ファイルがコンパイルされない
## 環境
- OpenJDK: 11.0.2
- JRuby: 9.2.12.0
- Rails: 6.0.3.3
- minitest: 5.1
- TypeScript: 4.0.2
- Vue.js: 2.6.12
## 起こった問題
TypeScript と Vue.js をプロジェクトにインストールして、簡単に要素を記述してレンダリング。  
その後、minitest の システムテストを実行したときに下記のようなエラーが発生した。

<details>
<summary>エラーログ</summary>

```shell
Error:
HomeTest#test_index_page_displays_category:
ActionView::Template::Error: Webpacker can't find hello_vue in /Users/takahashikouhei/dev/tsunade_ui/public/packs-test/manifest.json. Possible causes:
1. You want to set webpacker.yml value of compile to true for your environment
   unless you are using the `webpack -w` or the webpack-dev-server.
2. webpack has not yet re-run to reflect updates.
3. You have misconfigured Webpacker's config/webpacker.yml file.
4. Your webpack configuration is not creating a manifest.
Your manifest contains:
{
  "application.js": "/packs-test/js/application-31c0a7fd2aa09b742314.js",
  "application.js.map": "/packs-test/js/application-31c0a7fd2aa09b742314.js.map",
  "entrypoints": {
    "application": {
      "js": [
        "/packs-test/js/application-31c0a7fd2aa09b742314.js"
      ],
      "js.map": [
        "/packs-test/js/application-31c0a7fd2aa09b742314.js.map"
      ]
    }
  }
}
```

</details>

## 解決策

この問題は `public/packs-test` に本来生成されるはずの Vue.js と TypeScript 用のコンパイルされたファイルが生成されなかったことが原因だった。
ローカルの `public/packs-test` ディレクトリごと削除して、再度システムテストを走らせたところ、正常に上記のファイルが生成されて解決。

## 知ったところ
- 社内
