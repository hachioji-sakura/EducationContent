### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 最初の材料の検出

## ステップ 1
エージェントは**金**ブロックを**破壊**し、その後**収集**する必要があります。 

```template
player.onChat("material", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(LEFT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == GOLD_BLOCK) {
            
        }
    }
})
```

```ghost
player.onChat("1", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(LEFT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == GOLD_BLOCK) {
            agent.destroy(FORWARD)
            agent.collectAll()
        }
    }
})
```



