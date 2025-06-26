### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムしてすべてのゴミを回収させよう！

## ステップ 1
``||agent:エージェント破壊||``と``||agent:エージェント全回収||``ブロックを使用して、カメの足跡をきれいにするためにエージェントを使用します。``||loops:くりかえし||``ブロックを使用してコードをより効率的にしてみてください。完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftでコードを実行することを忘れないでください。 


```ghost
player.onChat("garbage", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```
