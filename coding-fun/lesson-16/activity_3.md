### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# タウンホールを建てよう！

## ステップ 1
**石**を建材として使用し、**3**つの``||variables: 変数||``を作成し、それらに**幅**、**長さ**、**高さ**という名前を付けます。``||variables: 変数||``を正しいパラメータに設定することを忘れないでください。変数を``||player: チャット時||``コマンドに追加するのを忘れないでください。

```ghost
// run 5 10 12
player.onChat("town_hall", function (length, width, height) {
    for (let index = 0; index < height; index++) {
        for (let index = 0; index < 2; index++) {
            for (let index = 0; index < length; index++) {
                agent.setItem(STONE, 1, 1)
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
            for (let index = 0; index < width; index++) {
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
