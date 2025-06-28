### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ローバーを修理せよ

## ステップ 1
現在のコードを修正してください。目標は次のとおりです：  
1. **空気**のブロックを**検査**し、それが**見つからない**間、エージェントは**右に移動**する必要があります。
2. エージェントが**前方**に**ラピスラズリ**ブロックを見つけた場合、**右に移動**、**左回転**してから**右に移動**する必要があります。
3. その後、エージェントは「破損箇所を発見！」と言い、**前方にレッドストーンブロックを設置**する必要があります。



```template
player.onChat("repair", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) == AIR) {
        agent.move(RIGHT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == LAPIS_LAZULI_BLOCK) {
            agent.move(RIGHT, 1)
            agent.turn(RIGHT_TURN)
            agent.move(LEFT, 1)
        }
    }
    player.say("Found the break!")
    agent.setItem(GRASS, 1, 1)
    agent.place(FORWARD)
})
```
