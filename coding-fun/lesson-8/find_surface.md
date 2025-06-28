### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# マグマに到達

## ステップ 1
エージェントが**前進**するようにプログラムします。もし、エージェントの**下**のブロックが**マグマではない**間、エージェントは**下に移動**する必要があります。 


```ghost
player.onChat("magma", function () {
    agent.move(FORWARD, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != MAGMA_BLOCK) {
        agent.move(DOWN, 1)
    }
})
```

