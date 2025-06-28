### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 恐竜をすり抜けよう！

## ステップ 1
自分を``||mobs:透明||``にして恐竜を``||player:スニーク||``してすり抜ける必要があります。これを実現できますか？

### ~ tutorialHint
Minecraftでこそこそ移動するには、ShiftとWを押してみてください。

```ghost
player.onTravelled(SNEAK, function () {
    mobs.applyEffect(INVISIBILITY, mobs.target(NEAREST_PLAYER), 3, 1)
})
```
