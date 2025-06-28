### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 周囲の探索

## ステップ 1
**氷塊**である**下のブロックを検査**している間、エージェントが**右のブロックを検出**した場合、**前進**する必要があります。そうでなければ**右に移動**する必要があります。



```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == PACKED_ICE) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.move(FORWARD, 1)
        } else {
            agent.move(RIGHT, 1)
        }
    }
})
```

