### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# エリアをきれいにしよう！

## ステップ 1
隠れ家の**4辺**に沿って**14個のタンポポ**を植える必要があります。``||loops:くりかえし||``ブロックを2つ使用して、タンポポを植えましょう。
- 1つ目の``||loops:くりかえし||``ブロックで、14回タンポポを置きます
- くりかえしの最後で**右**に方向転換します
- 上記のコードを4回くりかえします

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
