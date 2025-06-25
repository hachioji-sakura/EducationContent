### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# 高い場所！

## ステップ 1
**オーク**ブロックで**10**ブロックの高さのタワーを建設するようにエージェントをプログラムします。まず、``||agent:ブロックまたはアイテムを設定||``コマンドを使用して、エージェントが**オークの板**を**64**ブロック持っていることを確認します。``||agent:エージェント設置||``ブロックを使用して、オークの板を**前方**、**左**、**右**に配置するようにエージェントをプログラムします。エージェントはブロックを置いた後、**上に移動**する必要があります。

#### ~ tutorialhint 
``||loops:繰り返し||``ブロックを使用して数字を**10**に変更してみてください。

## ステップ 2
エージェントがタワーから**下に移動**し、**10**ブロックの高さの**はしご**を建設するようにプログラムします。登ることができるようにはしごが必要です！

#### ~ tutorialhint 
エージェントがはしごを設置できるように、``||agent:エージェントブロック設定||``を使用してエージェントのインベントリに**はしご**を**64**ブロック選択することを忘れないでください。


```ghost
player.onChat("tower", function () {
    agent.move(FORWARD, 1)
    agent.setItem(LADDER, 64, 1)
    for (let index = 0; index < 10; index++) {
        agent.place(FORWARD)
        agent.move(UP, 1)
    }
    agent.move(DOWN, 10)
})

``` 


