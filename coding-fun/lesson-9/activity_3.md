### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ローバーを追跡せよ

## ステップ 1
このコードスニペットを修正してください。目標は次のとおりです：  
1. **前方を検査**して**クォーツ**ブロックを探し、それが**見つからない**間、エージェントは**前進**する必要があります。
2. **下**に**金**ブロックを**検出**した場合、**右回転**する必要があります。
3. **下**に**鉄ブロック**を検出した場合、**左回転**する必要があります。
4. 最後に、エージェントは「ローバーを発見！」と言う必要があります。




```template
player.onChat("rover", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != BLOCK_OF_QUARTZ) {
            if (agent.inspect(AgentInspection.Block, UP) == GOLD_BLOCK) {
            agent.turn(LEFT_TURN)
        }
            if (agent.inspect(AgentInspection.Block, RIGHT) == IRON_BLOCK) {
            agent.turn(RIGHT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the rover!")
})
```

