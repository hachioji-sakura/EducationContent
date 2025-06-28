### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 鉄

## ステップ 1
もし、エージェントの**下のブロック**が、**鉄鉱石ではない**間、**前進**する必要があります。また、エージェントが**前にブロックを検出**した場合、**前を破壊**する必要があります。エージェントが鉄を見つけたら、それを**収集**するようにプログラムします。

```ghost
player.onChat("4", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != IRON_ORE) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the iron ore!")
    agent.destroy(DOWN)
    agent.collectAll()
})
```
