### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 深層の石

## ステップ 1
現在のコードを修正してください。エージェントの目標は次のとおりです：**左**に**金**ブロックが見つかるまで地表を掘り下げます。下降中に、エージェントは前方に**石**があるかどうかを検出し、あればそれを収集します。

```template
player.onChat("dig", function () {
    while (agent.inspect(AgentInspection.Block, LEFT) == AIR) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
            if (agent.inspect(AgentInspection.Block, FORWARD) != GRASS) {
                player.say("Found the stone!")
                agent.destroy(FORWARD)
                agent.collectAll()
        }
    }
})
```


