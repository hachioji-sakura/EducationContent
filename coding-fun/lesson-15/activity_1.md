### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# クォーツ採掘！

## ステップ 1
残りの柱を建設するために必要な**ブロック**数を**計算**するコードを書いてください。事実は次のとおりです：**6本の柱**があり、各柱の高さは**6ブロック**です。まず、``||loops:開始時||``に``||variable:高さ||``と``||variable:数量||``変数を作成して正しい数字に設定し、次に``||variable:合計ブロック||``変数を作成します。

## ステップ 2
条件を設定し、``||variable:合計ブロック||`` = ``||variable:高さ||`` * ``||variable:数量||``の場合、``||logic:もし||``文で「十分なブロックが集まりました！」と``||player:言う||``ようにします。

## ステップ 3
今度は``||variable:合計ブロックを1変更||``コマンドと``||variable:合計ブロック||``を``||player:言う||``を追加して、収集したブロック数を把握できるようにします。ブロックを破壊している間にカウントが表示されるように、``||blocks:クォーツ柱ブロックが壊された時||``を追加してください。完了すると、「十分なブロックが集まりました！」というメッセージが表示されます。

```ghost
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
