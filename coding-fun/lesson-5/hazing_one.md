
### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# 追い払い その1

2つのトリップワイヤーフックの間を、トリップワイヤーでつなぎ合わせるプログラムを書きましょう。

## ステップ 1
``||agent:エージェント ブロック設定||``を**トリップワイヤー**に設定し、**64**個のトリップワイヤーをエージェントに渡します。

## ステップ 2
``||loops:もし～ならくりかえし||``ブロックを使用し、``||loops:もし～ならくりかえし||``ブロックの中に条件を入れます。

#### ~ tutorialhint

```blocks
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
## ステップ 3
``||loops:もし～ならくりかえし||``ブロックの中に``||agent:置かせる||``と``||agent:移動させる||``ブロックを追加します。

```blocks
player.onChat("run", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```