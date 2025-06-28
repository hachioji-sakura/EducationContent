### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# サンプルを見つけよう！

## ステップ 1
もし、エージェントの**下のブロック**が、**青氷でない**間、エージェントが**破壊**して**下に移動**するようにプログラムします。エージェントが**青氷**を見つけたら、**下を破壊**してサンプルを**収集**する必要があります。 

```ghost 
player.onChat("ice", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != ICE) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
    }
    agent.destroy(DOWN)
    agent.collectAll()
    
})
```

