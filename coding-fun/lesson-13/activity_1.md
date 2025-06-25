### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 溶岩遊泳

## ステップ 1
あなたの課題は溶岩湖を``||player:泳いで||``渡ることです。**最も近いプレイヤー**に``||mobs:耐火性を適用||``してみてください。



```ghost
player.onTravelled(SWIM_LAVA, function () {
    mobs.applyEffect(FIRE_RESISTANCE, mobs.target(NEAREST_PLAYER), 10, 1)
    mobs.clearEffect(mobs.target(NEAREST_PLAYER))
})
```
