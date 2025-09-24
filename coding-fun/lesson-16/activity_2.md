### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# スターターハウスを建てよう！

## ステップ 1
heightは高さ、sizeは幅を表します。

今あるサンプルコードは、size個のブロックを前1列に配置します。家の囲いを作る必要があるため、それを**4回**繰り返す必要があります。

次に``||agent: エージェントを上に移動||``し、全体を``||variables: height||``の回数ぶん、``||loops: 繰り返し||``をします。

このコードを使用すると、**1**つの家を建てることができます。

### ~ チュートリアルヒント
コマンドを入力する際には、ゲーム内チャットで数字を入力するのを忘れないでください。例えば、**house 2 5**のように。

```template    
 player.onChat("house", function (height, size) {
    for (let index = 0; index < size; index++) {
        agent.setItem(STONE, 1, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```

```ghost
// 左の家は、house 3 4
// 右の家は、house 5 4
player.onChat("build-simple", function (size, height) {
    for (let index = 0; index < height; index++) {
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < size; index++) {
                agent.setItem(STONE, 1, 1)
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})
```



