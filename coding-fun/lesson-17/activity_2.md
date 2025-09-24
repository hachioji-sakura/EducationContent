### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# タウンホールを建てよう！

## ステップ 1
**plantSeed**という関数を作成しました。これは、前のアクティビティで使用したコードです。今、``||player: チャットコマンド||``をワークスペースにドラッグし、名前を**run**にします。``||loops: 繰り返し||``ループを追加し、**高度なブロック**をクリックしてから**関数**をクリックし、``||function:call plantSeed||``関数をループにドラッグします。エージェントが**plantSeed**関数を繰り返す必要がある回数を数えて入力し、実行してください。

### ~ tutorialhint
関数は**高度な**セクションにあります。書かれたコードについてのメモを残すことも良い習慣です。これは、関数についてあなたのために残したものと同じです。 

```template
/**
 * A function allows you to easily reuse code.
 */
function plantSeed () {
    agent.till(FORWARD)
    agent.move(FORWARD, 1)
    agent.place(DOWN)
}
```

```ghost
player.onChat("plantSection", function () {
    for (let index = 0; index < 11; index++) {
        plantSeed()
    }
    agent.move(FORWARD, 1)
})
```
