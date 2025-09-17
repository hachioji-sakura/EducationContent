### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 建築

## ステップ 1
最初だけ、**34個の鉄**ブロックを自分に``||mobs:与えて||``ください。
次に、新しい``||variables:変数||``を作成し、**count**と名前を付けます。

``||blocks:ブロックが置かれた時||``ブロックを取得し、**鉄**に設定します。ここに、``||変数を増やす||``ブロックおよび、``||player:メッセージを送信する||``ブロックを追加します。``||player:メッセージを送信する||``ブロックの中に``||count||``を追加します。これにより、ブロックを配置するたびに、ゲームが配置したブロックの数をカウントすることができます。

### ~ tutorialhint 

鉄、金、エメラルド、またはダイヤモンドを選択できます。

```blocks
let count = 0
blocks.onBlockPlaced(EMERALD_BLOCK, function () {
    count += 1
    player.say(count)
})

```

```ghost
blocks.onBlockBroken(STONE, function () {
    count += 1
    player.say(count)
})
let count = 0
mobs.give(
mobs.target(NEAREST_PLAYER),
STONE,
34
)
```


