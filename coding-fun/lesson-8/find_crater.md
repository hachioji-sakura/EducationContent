### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 周囲の探索

## ステップ 1
エージェントの**下にブロックがある**間、前進する必要があります。もし、エージェントの**下のブロックが空気**である場合、``||player:送信する||``コマンドを使用して**クレーターを発見！**と言います。 



```template
player.onChat("crater", function () {
            player.say("Crater found!")
})
```
```ghost
player.onChat("1", function () {
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(FORWARD, 1)
    }
    if (agent.inspect(AgentInspection.Block, DOWN) == AIR) {
        player.say("Crater found!")
    }
})
```