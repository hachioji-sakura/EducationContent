### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 家畜

## ステップ 1
初期コードを見て実行してみてください。このコードを使うと、ブロックを数えずにエージェントを操作できます。エージェントが通る必要のある道を見て、エージェントの向きを正しく変更してください。エージェントが**金のプレート**に到達できることを確認してください。  

```template
player.onChat("sheep", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

``` 

