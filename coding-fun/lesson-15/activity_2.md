### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# 柱！

## ステップ 1
水道橋を建設する時間です！まず、``||variable:長さ||``と``||variable:セグメント||``変数を作成します。次に、``||loops:開始時||``に``||variable:長さを設定||``を**5**に、``||variable:セグメントを設定||``を**6**に設定します。

## ステップ 2
次に、``||player:チャットコマンド時||``の中で、エージェントが**1**つの部分を建設するために実行する必要のあるすべてのアクションを追加します：``||agent:クォーツの柱ブロックを設定||``を**64**個、``||agent:設置||``と``||agent:前進||``。Minecraftでは、傾斜があると水が流れるため、エージェントは**左、右、下に設置**する必要があります。これらのアクションをすべて``||variable:長さ||``回数**繰り返す**``||loops:くりかえし||``ループの中に配置します。

## ステップ 3
次に、最初の``||loops:くりかえし||``ループを、``||variables:セグメント||``回数繰り返す別の``||loops:くりかえし||``ループの中にネストします。Minecraftで試してみてください！

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
