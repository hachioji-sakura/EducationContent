### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# 美しいもの！

## ステップ 1
あなたの任務は、浴場の床の境界に沿って**クォーツの柱**と**ラピスラズリ**ブロックの交互パターンを作ることです。まず、``||variable:ブロックA||``と``||variable:ブロックB||``変数を作成します。``||variable:ブロックA変数||``を**クォーツブロック**に、``||variable:ブロックB変数||``を**ラピスラズリブロック**に設定します。コマンドを``||loops:開始時||``ブロックに追加します。

## ステップ 2
``||logic:もし||`` ``||count||`` = **0**の場合、エージェントは``||variable:ブロックA||``を設定し、``||agent:下を破壊||``、``||agent:下に設置||``して``||variable:カウントを1変更||``する必要があります。``||logic:そうでなければ||``エージェントは``||ブロックB||``を設定し、ブロックを設置して``||カウントを-1変更||``する必要があります。

## ステップ 3
エージェントは**前方**のブロックを``||logic:検出しない||``間、``||loops:もし～ならくりかえし||``でブロックを一列に配置する必要があります。

## ステップ 4
エージェントが完成させる必要のある貯水池の**4**つの辺があるため、``||loops:くりかえし||``ブロックを追加します。エージェントをブロック配置に送る前に``||count||``を**0**に設定します。

```template
let count = 0
player.onChat("floor", function () {
    count = 0
})
```


```ghost
player.onChat("floor", function () {
    count = 0
    for (let index = 0; index < 4; index++) {
        while (!(agent.detect(AgentDetection.Block, FORWARD))) {
            if (count == 0) {
                agent.setItem(blockA, 1, 1)
                agent.destroy(DOWN)
                agent.place(DOWN)
                count += 1
            } else {
                agent.setItem(blockB, 1, 1)
                agent.destroy(DOWN)
                agent.place(DOWN)
                count += -1
            }
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})
let count = 0
let blockB = 0
let blockA = 0
blockA = BLOCK_OF_QUARTZ
blockB = LAPIS_LAZULI_BLOCK
```
