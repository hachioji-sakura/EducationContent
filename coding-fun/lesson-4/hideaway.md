### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 竹の隠れ家

## ステップ 1
砂の区画の全ての辺に**3**ブロックの竹を植えるようにエージェントをプログラムします。

#### ~ tutorialhint
2つの**くりかえし**ループが必要で、一方を他方の内側に入れる必要があります。
 
```ghost
player.onChat("bamboo", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```


