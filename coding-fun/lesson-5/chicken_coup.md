### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 鶏小屋

## ステップ 1
エージェントは**鉄格子**の**9**ブロックを**2**層配置する必要があります。**鉄格子**が必要な**4**辺があります。2階層目を建設するために``||agent:エージェントを上に移動||``を使用することを忘れないでください。

#### ~ tutorialhint
最終的に3つの``||loops:くりかえし||``が入れ子になっています。エージェントのインベントリに64ブロック以上あることを確認してください！

```ghost
player.onChat("chicken", function () {
    for (let index = 0; index < 2; index++) {
        agent.setItem(IRON_BARS, 1, 1)
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 9; index++) {
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})

``` 
