### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 大峡谷！

## ステップ 1
氷の峡谷を渡る**橋を建設**するようにエージェントをプログラムします。``||agent:ブロックまたはアイテムを設定||``を使用して、エージェントに必要な材料を渡します。建築材料として**オーク**を選択し、**ブロック数**に**64**を設定します。エージェントが下にブロックを**検出しない**間、``||loops:もし～ならくりかえし||``を使用して、オークの板を**下**に置き、**前進**して橋を作るようにエージェントをプログラムします。

```template
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 1, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, DOWN))) {
    	
    }
})
```

```ghost
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})

``` 

