### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 周囲の探索

## ステップ 1
**氷塊ではない**下のブロックを**検査**している間、エージェントが**右のブロックを検出**した場合、**前進**する必要があります。そうでなければ**右に移動**する必要があります。同じループ内で、エージェントが**下のブロックを検査**し、それが**石**または**砂利**の場合、**下を破壊**して**すべて収集**する必要があります。 



```template
player.onChat("ice", function () {
    while (0 == 0) {
        if (true) {
        	
        } else {
        	
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE ||agent.inspect(AgentInspection.Block, DOWN) == GRAVEL ) {
        	
        }
    }
})
```
```ghost
player.onChat("2", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != PACKED_ICE) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.move(FORWARD, 1)
        } else {
            agent.move(RIGHT, 1)
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE || agent.inspect(AgentInspection.Block, DOWN) == GRAVEL) {
            agent.destroy(DOWN)
            agent.collectAll()
        }
    }
})
```
