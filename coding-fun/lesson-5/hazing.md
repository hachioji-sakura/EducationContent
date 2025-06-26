### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 追い払い

## ステップ 1
オオカミが入らないようにエージェントに**トリップワイヤー**を設置させる必要があります。``||agent:エージェント ブロック設定||``を**トリップワイヤー**に設定し、個数を**64**に設定します。``||loops:もし～ならくりかえし||``ブロックを使用し、その中に条件を入れます。

#### ~ tutorialhint
条件で**ではない**を使用することを忘れないでください。

```blocks
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
```ghost
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```
