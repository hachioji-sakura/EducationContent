### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# スターターハウスを建てよう！

## ステップ 1
提供されたサンプルコードを使用して、1行のブロックを配置します。その後、エージェントは同じ手順を**4回**繰り返し、次に``||agent: 上に移動||``し、さらに繰り返します。``||variable: 高さ||``を取得し、それを``||loops: 繰り返し||``ブロックに追加します。このコードを使用すると、**1**つの家を建てることができます。

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



