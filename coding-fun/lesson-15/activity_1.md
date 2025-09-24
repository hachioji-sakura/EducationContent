### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# クォーツ採掘！

## ステップ 1
残りの柱を建設するために必要なブロック数を計算するコードを作成します。

変数は、``||variables:高さ||``と``||variables:数量||``、``||variables:合計||``の3つを使います。

まず、**6本の柱**があり、各柱の高さは**6ブロック**です。よって、``||loops:最初だけ||``に、``||variables:高さ||``と``||variables:数量||``変数をそれぞれ6に設定します。

## ステップ 2
次に、必要なブロックの数を数えるコードを書きます。

まず、``||blocks:柱状のクォーツブロックが壊された時||``を追加します。
``||variables:合計を1だけ増やす||``ブロックを使用して、破壊された合計の数を数えましょう。



## ステップ 3
最後に、必要なクォーツブロックの数が集まったかどうかを通知するコードを書きます。

``||logic:もし||``を使い、``||variables:合計||`` = ``||variables:高さ||`` × ``||variables:数量||``の場合、「十分なブロックが集まりました！」と``||player:メッセージを送信する||``ようにします。


```ghost
# もしかしたら、「を破壊した時」ブロックが使えないかもしれない。
# 問題に取り組む前に生徒に、柱状のクォーツブロックを破壊した時メッセージを送信するという簡易的なコードを書かせて、動くかどうかを確認する。

blocks.onBlockBroken(PILLAR_QUARTZ_BLOCK, function () {
    total_blocks += 1
    if (total_blocks == height * quantity) {
        player.say("Collected enough blocks!")
    }
})
let total_blocks = 0
let quantity = 0
let height = 0
height = 6
quantity = 6
```
