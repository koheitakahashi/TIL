# Unix・Linuxの終了ステータス
## 終了ステータスとは?
Unix・Linuxでは、コマンド終了時にexit-statueと呼ばれるコマンドの成否を表す数値が特殊変数`$?`に自動で設定されます。

一般的にコマンド成功時には「0」・失敗時には「1」が設定されています。

exit-statusは以下のようにすることで確認できます。

```shell
(なんらかのコマンド実行後に)
echo $?
```

## 学んだところ
- 社内
- [終了ステータス \| UNIX & Linux コマンド・シェルスクリプト リファレンス](https://shellscript.sunone.me/exit_status.html) 
