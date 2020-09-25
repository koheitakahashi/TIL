# privateなclass_methodを定義する
## 方法
以下のように書くと、privateなclass methodを定義することができます。  
また、まとめてclass methodを定義したい時にも便利です。

```ruby
class Hoge

  class << self
    def foo
    end

    private
      def hogefoo
      end
  end
end

```

## 学んだところ
[Sendagaya\.rb \#329](https://sendagayarb.doorkeeper.jp/events/111583)

