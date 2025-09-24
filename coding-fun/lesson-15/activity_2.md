### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# 柱！

## ステップ 1
水道橋を建設する時間です！まず、``||variables:長さ||``と``||variables:セグメント||``変数を作成します。次に、``||loops:最初だけ||``に``||variables:長さ||``を**5**に、``||variables:セグメント||``を**6**に設定します。

## ステップ 2
次に、``||player:チャットコマンド時||``を使い、橋を建設します。

``||agent:クォーツの柱ブロックを設定||``を**64**個、エージェントは**左、右、下に設置**して**前に進む**ことを、``||variables:長さ||``回数``||loops:くりかえす||``必要があります。

Minecraftでは、傾斜があると水が流れるため、エージェントを**下**移動させることを忘れないでください。

## ステップ 3
次に、最初の``||loops:くりかえし||``ループを、``||variables:セグメント||``回数繰り返す別の``||loops:くりかえし||``ループの中に内包します。Minecraftで試してみてください！

### ~ tutorialHint
コードが動作するように、内側のループの前に``||agent:エージェント下移動||``ブロックを追加してください！

```ghost
player.onChat("build", function () {
    agent.move(DOWN, 1)
    for (let index = 0; index < Segments; index++) {
        for (let index = 0; index < length; index++) {
            agent.setItem(WHITE_CONCRETE, 64, 1)
            agent.place(LEFT)
            agent.place(RIGHT)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 1)
    }
})
let Segments = 0
let length = 0
length = 5
Segments = 6
```
