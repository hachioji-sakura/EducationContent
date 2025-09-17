### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 雨を降らせよう！

## ステップ 1
Minecraftでダンスしながら雨を降らせましょう！これを実現するには、いくつかのイベントハンドラーを使用する必要があります。

1. 変数を作成します（例：**walk**、**jump**、**break**）。
2. イベントハンドラーを選択します（例：``||player:プレイヤーが落下した時||``、``||player:プレイヤーが歩いた時||``）。
3. 対応する各イベントブロック内で新しい``||variables:変数||``を``||logic:真||``に設定します。
4. ``||loops:ずっと||``ブロックを使用し、その中に``||logic:もし〜なら||``をドラッグします。もし全ての変数が``||logic:真||``なら、``||gameplay:天気||``を**雨**に設定します。

### ~ tutorialHint
```blocks
let walk = false
player.onTravelled(WALK, function () {
    walk = true
})
loops.forever(function () {
    if (walk == true && "" == "") {
    	
    }
})

```

```ghost
let climb = false
let walk = false
let _break = false
player.onTravelled(CLIMB, function () {
    climb = true
})
player.onTravelled(WALK, function () {
    walk = true
})
blocks.onBlockBroken(STONE, function () {
    _break = true
})
loops.forever(function () {
    if (walk == true && climb == (true && _break == true)) {
        gameplay.setWeather(RAIN)
    }
})
```
