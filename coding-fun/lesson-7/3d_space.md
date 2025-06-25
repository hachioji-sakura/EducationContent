### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 3D空間

## ステップ 1
この課題を解決するには、エージェントが**金**ブロックに到達して収集するようにプログラムする必要があります。エージェントは最初に地面レベルでこれを行い、その後**3レベル上に移動**して前の手順を繰り返す必要があります。  

```template
player.onChat("3D", function () {
    for (let index = 0; index < 2; index++) {
        
})
``` 
```ghost
player.onChat("3D", function () {
    for (let index = 0; index < 2; index++) {
        while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
            if (!(agent.detect(AgentDetection.Block, FORWARD))) {
                agent.move(FORWARD, 1)
            } else {
                agent.turn(LEFT_TURN)
            }
        }
        agent.destroy(FORWARD)
        agent.collectAll()
        agent.move(UP, 3)
    }
})
```