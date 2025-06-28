### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ポータルに電力を供給しよう！

## ステップ 1
**金ブロック**の上に立っている間に雷を落とす必要があります。まず、``||loops:最初だけ||``に``||gameplay:天気||``を雨に設定する必要があります。次に、``||player:プレイヤーが歩いた時||``の中に``||logic:もし||``、足元に``||blocks:金ブロックが存在する||``なら、``||mobs:ライトニングボルト||``を配置して、正確なタイミングで雷を落とします。 

### ~ tutorialHint
金のプレートはあなたの足元の**0, -1, 0**座標にあります。 

```ghost
player.onTravelled(WALK, function () {
    if (blocks.testForBlock(GOLD_BLOCK, pos(0, -1, 0))) {
        mobs.spawn(LIGHTNING_BOLT, pos(0, 0, 0))
    }
})
gameplay.setWeather(RAIN)
```
