### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 周囲の検知

## ステップ 1
エージェントが**下のブロックを検査している**間、そのブロックが**石**である場合、エージェントは**前進**する必要があります。エージェントが前方にブロックを**検出しない**場合は**前進**する必要があり、そうでなければ**左折**する必要があります。 


```template
player.onChat("inspect", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        
    }
})
```

```ghost
player.onChat("inspect", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
})
```

