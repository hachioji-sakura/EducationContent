### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 離ればなれの家族！

## ステップ 1
氷の峡谷を渡る橋を建設するようにエージェントをプログラムします。まずは、エージェントに**オークの板**を**64**ブロック渡します。



#### ~ tutorialhint 
**くりかえし**ループで**ではない**を使用することを忘れないでください。エージェントにブロックを置きたい場所を考えてください。


```ghost
player.onChat("family", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
})

``` 
