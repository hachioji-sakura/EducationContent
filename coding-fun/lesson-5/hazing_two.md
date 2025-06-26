### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# 追い払い その2

## ステップ 1
ステップ1は追い払いその2を実行することです。

## ステップ 2
完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftでコードを実行することを忘れないでください。

```blocks
player.onChat("run", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

``` 
