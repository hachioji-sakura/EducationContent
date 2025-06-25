### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムしてカメの足跡に沿って移動し、障害物を破壊させよう！

## ステップ 1
``||agent:エージェント破壊||``と``||agent:エージェント全回収||``ブロックを使用して、邪魔になっている**木の幹を破壊**するためにエージェントを使用します。``||loops:繰り返し||``ブロックを使用してコードをより効率的にしてみてください。完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftでコードを実行することを忘れないでください。 


```ghost
player.onChat("path", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
``` 

