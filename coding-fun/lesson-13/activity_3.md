### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 建築

## ステップ 1
少なくとも**34個のエメラルド**ブロックを自分に``||mobs:与えて||``ください。新しい``||variable:変数||``を作成し、**count**と名前を付けます。``||blocks:ブロックが置かれた時||``ブロックを取得し、**エメラルド**に設定します。``||変数を増やす||``ブロックを``||blocks:ブロックが置かれた時||``の中にドラッグし、``||player:メッセージを送信する||``ブロックを追加します。``||player:メッセージを送信する||``ブロックの中に``||count||``を追加します。これにより、ブロックを配置するたびに、ゲームが配置したブロックの数をカウントします。

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
1
)
})
```


