### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# スパイラル

## ステップ 1
エージェントが**前方のブロックを検査している**間、そのブロックが**金ブロックではない**場合、エージェントは**前進**する必要があります。エージェントが前方にブロックを**検出しない**場合も前進する必要があり、そうでなければ**左折**する必要があります。エージェントが**金ブロック**に到達したら、それを**破壊**して**収集**する必要があります。 


```ghost
player.onChat("3", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
    agent.destroy(FORWARD)
    agent.collectAll()
})
```
