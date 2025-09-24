### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1



# ビートを植えよう！

## ステップ 1

2つの関数**plantSeed**と**plantSection**が提供されています。

新しい``||player:チャットコマンド||``を作成し、その中で``||functions:plantSectionを呼び出し||``ます。

``||logic:もし||``、``||agent:エージェントの下のブロック||``が ``||blocks:ラピスラズリ||``の場合、エージェントは``||agent:右に回転||``、``||agent:前進||``、``||agent:右に回転||``する必要があります。  

``||logic:もし||``、``||agent:エージェントの下のブロック||``が ``||blocks:ラピスラズリ||``の場合、エージェントは``||agent:左に回転||``、``||agent:前進||``、``||agent:左に回転||``する必要があります。  

最後に``||functions:plantSectionを呼び出し||``ます。

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
})
```

```template
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}

function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    agent.place(DOWN)
}

```


```ghost
player.onChat("turn", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    }
    plantSection()
})
```

