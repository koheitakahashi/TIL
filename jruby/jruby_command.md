# JRubyの起動時間を短縮するコマンド
## `jruby --dev -S`
`jruby --dev -S`を実行したいコマンドの前につけると、JRubyの実行時間が短縮されます。  

`--dev`フラグは、JVMを速度重視のモードで起動するフラグです。  
`-S`オプションは、その後ろのコマンドやスクリプトを実行するためのオプションです。

以下のように使うことができます。

```shell
jruby --dev -S bin/rails s
```

## 学んだところ
- 社内
- [jruby Improving startup time Use the "--dev" flag](https://github.com/jruby/jruby/wiki/Improving-startup-time#use-the---dev-flag)
- `jruby -h`

