### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ホロデッキ

## ステップ 1
このホロデッキを使用してスキルを磨きましょう！ 

```ghost
player.onChat("3", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
    agent.destroy(FORWARD)
    agent.collectAll()
    agent.setItem(GRASS, 1, 1)
agent.place(FORWARD)
agent.till(FORWARD)
agent.collect(IRON_SHOVEL)
agent.setSlot(1)
agent.transfer(1, 1, 2)
})
```
