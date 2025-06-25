### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 世界を変えよう！

## ステップ 1
``||player:プレイヤーが歩いた時||``イベントを使用して、特定の``||positions:ワールド||``座標（**100, 68, 100**）にブロックを設置します。``||variable:変数||``を作成し、**count**と名前を付けます。``||countを1増やす||``ブロックと``||count||``変数を追加した``||blocks:置く||``ブロックをドラッグします。これにより1ずつ増加し、そのブロックIDに関連付けられたブロックが設置されます。1=石、2=草、3=土、など。別のイベントブロック（例：``||player:プレイヤーが落下した時||``）を使用してブロックをリセットします。そのために、``||countを設定||``を**0**にドラッグしてカウントを再開し、同じワールド座標に設定された``||variable:count||``変数を追加した``||blocks:設置||``ブロックを追加します。これにより、ワールドでジャンプするたびに、ブロックがリセットされます。

### ~ tutorialhint 
座標を示すために``||positions:ワールド||``位置を使用することを忘れないでください。

```blocks
let count = 0
player.onTravelled(WALK, function () {
    count += 1
    blocks.place(count, world(100, 68, 100))
})
```

```ghost
let count = 0
player.onTravelled(WALK, function () {
    count += 1
    blocks.place(count, world(100, 68, 100))
})
player.onTravelled(FALL, function () {
    count = 0
    blocks.place(count, world(100, 68, 100))
})
```

