### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1



# ビートを植えよう！

## ステップ 1

2つの関数**plantSeed**と**plantSection**が提供されています。新しい``||player:チャットコマンド時||``を作成し、その中で``||functions:plantSectionを呼び出し||``ます。``||agent:エージェントが下のブロックを検査||``するかどうかを確認する``||logic:もし||``文を追加します。  
下のブロックが``||blocks:ラピスラズリ||``の場合、エージェントは``||agent:右に回転||``、``||agent:前進||``、``||agent:右に回転||``する必要があります。  
``||logic:そうでなければ||``エージェントが``||agent:下のブロックを検査||``して、それが``||blocks:クォーツブロック||``の場合、エージェントは``||agent:左に回転||``、``||agent:前進||``、``||agent:左に回転||``する必要があります。  
最後に``||functions:plantSectionを呼び出し||``ます。

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
})
```

```template
/**
 * 関数の中で関数を呼び出しています
 */
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}
 /**
 * エージェントの下にブロックがない場合は種を植えないようにコードを修正しました。
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    if (agent.detect(AgentDetection.Block, DOWN)) {
        agent.place(DOWN)
    }
}

/**
* エージェントがラピスブロックの上にいる場合は右に回転、クォーツの場合は左に回転するかどうかを確認する必要があります。
*/
```
## ステップ 2
``||player:チャットコマンド時||``に``||logic:もし||``文を追加します。``||logic:もし||``ブロックの**true**内に``||logic:" " = " "||``ブロックを追加します。``||agent:エージェントが下のブロックを検査||``が``||blocks:ラピスラズリ||``と**等しい (=)** 場合、エージェントは``||agent:右に回転||``、``||agent:前進||``、``||agent:右に回転||``する必要があります。

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    }

})
```

```template
/**
 * 関数の中で関数を呼び出しています
 */
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}
 /**
 * エージェントの下にブロックがない場合は種を植えないようにコードを修正しました。
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    if (agent.detect(AgentDetection.Block, DOWN)) {
        agent.place(DOWN)
    }
}

/**
* エージェントがラピスブロックの上にいる場合は右に回転、クォーツの場合は左に回転するかどうかを確認する必要があります。
*/
```

## ステップ 3
``||logic:もし||``ブロックの**+**記号を2回クリックします。** - **をクリックして**else**ブロックを削除します。``||logic:そうでなければもし||``ブロックの**空白**スペースに``||logic:" " = " "||``ブロックを追加します。``||agent:エージェントが下のブロックを検査||``が``||blocks:クォーツブロック||``と**等しい (=)** 場合。エージェントは``||agent:左に回転||``、``||agent:前進||``、``||agent:左に回転||``する必要があります。

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }

})
```

```template
/**
 * 関数の中で関数を呼び出しています
 */
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}
 /**
 * エージェントの下にブロックがない場合は種を植えないようにコードを修正しました。
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    if (agent.detect(AgentDetection.Block, DOWN)) {
        agent.place(DOWN)
    }
}

/**
* エージェントがラピスブロックの上にいる場合は右に回転、クォーツの場合は左に回転するかどうかを確認する必要があります。
*/
```

## ステップ 4
最後に、``||logic:もし||``文の外側の``||player:チャットコマンド時||``内に、もう一つの``||functions:plantSectionを呼び出し||``を追加します。

#### ~ tutorialhint
``` blocks
player.onChat("run", function () {
    plantSection()
    if (agent.inspect(AgentInspection.Block, DOWN) == LAPIS_LAZULI_BLOCK) {
        agent.turn(RIGHT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    } else if (agent.inspect(AgentInspection.Block, DOWN) == BLOCK_OF_QUARTZ) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
    plantSection()
})
```

```template
/**
 * 関数の中で関数を呼び出しています
 */
function plantSection () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
}
 /**
 * エージェントの下にブロックがない場合は種を植えないようにコードを修正しました。
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    if (agent.detect(AgentDetection.Block, DOWN)) {
        agent.place(DOWN)
    }
}

/**
* エージェントがどのブロックの上にいるかを確認する必要があります。ラピスブロックの上にいる場合は右に回転、そうでなければクォーツの場合は左に回転します。
*/

/**
* ifブロックの+ボタンをクリックしてElseを追加できます
*/

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

