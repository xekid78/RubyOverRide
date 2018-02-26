# RubyOverRide
メソッドのオーバーライド

## 処理
Boxクラスのopenメソッドを子クラスのMagicBoxクラスでオーバーライドする。

## コード
```
class Box
    def initialize(item)
        @item = item
    end

    def open()
        puts "宝箱を開いた。#{@item}を手に入れた。"
    end
end

class MagicBox < Box
    def look()
        puts "宝箱は怪しく輝いている"
    end

    def open()
        puts "宝箱を開いた。#{@item}が襲い掛かってきた。"
    end
end

box = Box.new("鋼鉄の剣")
box.open

magicBox = MagicBox.new("モンスター")
magicBox.look
magicBox.open
```

## 出力結果  
```
宝箱を開いた。鋼鉄の剣を手に入れた。
宝箱は怪しく輝いている
宝箱を開いた。モンスターが襲い掛かってきた。
```
  
## 開発環境
| 開発ツール |  |
|:-|:-|
| OS | Windows10 |
| 仮想化ソフト | Oracle VM VirtualBox 5.2 |
| 構築ソフト | Vagrant 2.0.2 |
| 仮想化上OS | CentOS 6.9 |
| SSHクライアント | PuTTY 0.6.8 |
| FTPクライアント | Cyberduck 6.3.5 |
| エディタ | Atom 1.24.0 |
| 開発言語 | Ruby 2.4.0 |
