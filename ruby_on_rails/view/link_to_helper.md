# link_to helperで生成されたリンクタグにclass属性をつけるときの注意点
## 問題となるコード
以下のように`link_to`ヘルパーを使ったときに、class属性をどのようにして指定するかというお話。
```ruby
link_to "リンクです", controller: "tasks", action: "index", search: { keyword: "仕事" }
```
## うまくいかない例
```ruby
link_to "リンクです", controller: "tasks", action: "index", search: { keyword: "仕事" }, class: "search-link"
# => class: "search-link" がクエリパラメーターだと解釈される
```
## うまくいく例
```ruby
link_to "リンクです", { controller: "tasks", action: "index", search: { keyword: "仕事" } }, class: "search-link"
```
