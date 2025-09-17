### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1

# 世界を変えよう！

## ステップ 1
まず、``||variables:変数||``を作成し、**count**と名前を付けます。

``||player:プレイヤーが歩いた時||``、``||count||``を1増やすようにします。また、``||count||``変数を``||positions:ワールド||``座標（**100, 68, 100**）に設置します。

ブロックは全てIDが割り当てられています（例、1=石、2=草、3=土、など。）。そのため、count変数を増やすことで、そのブロックIDに関連付けられたブロックが設置されます。

## ステップ 2
ブロックのリセットを行います。

別のイベントブロック（例：``||player:プレイヤーが落下した時||``）を使用してブロックをリセットします。``||countを設定||``を**0**し、先ほどと同様に``||variables:count||``を``||blocks:設置||``するブロックを追加します。

こうして、ワールドでジャンプするたびに、ブロックのIDが0にリセットされます。

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

