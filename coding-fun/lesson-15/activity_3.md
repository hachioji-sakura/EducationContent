### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# 美しいもの！

## ステップ 1
あなたの任務は、浴場の床の境界に沿って**クォーツの柱**と**ラピスラズリ**ブロックの交互パターンを作ることです。まず、``||variables:ブロックA||``と``||variables:ブロックB||``変数を作成します。``||variables:ブロックA変数||``を**クォーツブロック**に、``||variables:ブロックB変数||``を**ラピスラズリブロック**に設定します。コマンドを``||loops:最初だけ||``ブロックに追加します。

## ステップ 2
``||logic:もし||`` ``||variables:count||`` = **0**の場合、エージェントは``||variables:ブロックA||``を自分のスロットへ設定し、``||agent:下を破壊||``、``||agent:下に設置||``して``||variables:countを1だけ増やす||``必要があります。``||logic:そうでなければ||``エージェントは``||variables:ブロックB||``を設定し、ブロックを設置して``||variables:countを-1||``する必要があります。

## ステップ 3
``||agent:エージェントの前にブロックが||``、``||logic:ない||``間、``||loops:もし～ならくりかえし||``でブロックを一列に配置する必要があります。

エージェントは、前に進む必要があることを忘れないでください。

## ステップ 4
``||loops:くりかえし||``ブロックを使用して、貯水池の**4**つの辺を装飾できるようにしてください。

最初に``||variables:count||``を**0**に設定したら完成です。

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
