### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ビート！

## ステップ 1
あなたには、``||functions: plantSeed||``, ``||functions: plantSection||``、および``||functions: checkTurn||``の3つの関数が提供されています。まず、新しい``||player: チャット時||``コマンドを作成し、条件を追加します: ``||loops:while||`` エージェントが``||agent:下のブロックを検査||``していて、それが**金ブロック**でない限り、``||functions:呼び出す||``必要な関数を呼び出します。 


```template
/**
 * We are calling a function inside a function
 */
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}
 /**
 * The code was modified to not place seeds if there's no block under the Agent.
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    if (agent.detect(AgentDetection.Block, DOWN)) {
        agent.place(DOWN)
    }
}
function checkTurn () {
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
}

```


```ghost
player.onChat("plant", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != GOLD_BLOCK) {
        plantSection()
        checkTurn()
    }
})

function checkTurn () {
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
}

```
