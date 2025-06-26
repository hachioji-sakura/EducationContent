### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# エリアを確保しよう

## ステップ 1
**オークのフェンス**を建設するようにエージェントをプログラムします。エージェントは**オークのフェンス**ブロックを右に配置し、障害物を破壊して前進する必要があります。フェンスは**17ブロック**の長さにする必要があります。

#### ~ tutorialhint
エージェントが右にブロックを配置し、左のブロックを破壊することを確認してください。

```blocks
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
            }
})
```
```ghost
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
        agent.place(RIGHT)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
``` 

