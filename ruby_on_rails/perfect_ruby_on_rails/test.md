# 第7章 Railsアプリケーションのテスト
## テストヘルパー
- `Active::Support::Testing::TimeHelper#trave_to`(https://api.rubyonrails.org/classes/ActiveSupport/Testing/TimeHelpers.html#method-i-travel_to)
    - テストの中で現在の時刻を変更することができる。
## システムテストでしかできないこと
- ブラウザ上でJavaScriptの動作まで含めて確認
- フォームへ値を入力して登録する時の動作を確認
- 失敗した時の画面スクリーンショットを撮る
