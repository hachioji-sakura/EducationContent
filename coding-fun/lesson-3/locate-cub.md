### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 子熊を見つけよう！

## ステップ 1
``||loops:もし～ならくりかえし||``と``||agent:エージェントの前にブロックがある||``コマンドを使用して、どこまで続くか分からない道を掘るようにエージェントをプログラムします。雪の中をすべて歩けるように、エージェントは**前**と**上**を``||agent:破壊||``する必要があります。完了したら、**再生**ボタンを押してコードを実行します。

#### ~ tutorialhint 
ブロックを組み合わせるときのコードスニペットの形を見てください。``||agent:エージェントを移動させる||``を使用してください。

```template
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
    	
    }
})
```

```ghost
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

``` 
