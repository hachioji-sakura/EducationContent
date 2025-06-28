### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 石の位置特定

## ステップ 1
現在のコードを修正してください。

エージェントが実行する必要のあることは次のとおりです：  
1. **左に4回移動**、**下を破壊**、**下に移動**。
2. もし、エージェントが前方に**石**ブロックを検出した場合、「石を発見！」と言い、**前方を破壊**して**すべて収集**する必要があります。
3. 石が**検出されない**場合、エージェントは「ここには石がありません！」と言う必要があります。
4. 下に移動した後は毎回、エージェントは地表に**1ブロック上に移動**する必要があります。
5. この行動は、**4**回繰り返す必要があります。


```template
player.onChat("stone", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(RIGHT, 4)
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) != STONE) {
            player.say("Found the stone!")
            agent.destroy(FORWARD)
            agent.collectAll()
        } else {
            player.say("No stone here!")
        }
        agent.move(UP, 1)
    }
})
```
