### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# エリアをきれいにしよう！

## ステップ 1
隠れ家の**4辺**に沿って**14個のタンポポ**を植える必要があります。エージェントは片側に**14**個のタンポポを植えることができます。

#### ~ tutorialhint 
``||agent:エージェント ブロック設定||``コマンドのカウントを選択することを忘れないでください。


```ghost
player.onChat("flower", function () {
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 14; index++) {
            agent.setItem(YELLOW_FLOWER, 64, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})

``` 
