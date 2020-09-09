# migrationファイルで、SQLを実行するには？
## executeを使う
migrationファイルでSQLを実行したい場合には以下のように`execute`を使えます。
```ruby
def change
  add_column :tasks, :user_id, :bigint
  execute "UPDATE tasks SET user_id = (SELECT id FROM users  LIMIT 1);"
end
```
## 学んだところ
- 社内研修
- [Active Record マイグレーション \- Railsガイド](https://railsguides.jp/active_record_migrations.html#%E3%83%98%E3%83%AB%E3%83%91%E3%83%BC%E3%81%AE%E6%A9%9F%E8%83%BD%E3%81%A0%E3%81%91%E3%81%A7%E3%81%AF%E8%B6%B3%E3%82%8A%E3%81%AA%E3%81%84%E5%A0%B4%E5%90%88)
