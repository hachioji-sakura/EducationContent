### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 葉を取り除こう！

## ステップ 1
エージェントは**前方**に移動しながら**8**ブロックの葉を破壊する必要があります。エージェントが破壊する必要のある葉は**16**列あります。エージェントは``||agent:前を破壊||``と``||agent:前へ移動||``を**8**回実行する必要があります。 

#### ~ tutorialhint 
```blocks
player.onChat("foliage", function () {
    for (let index = 0; index < 8; index++) {
        for (let index = 0; index < 8; index++) {
        	
        }
    }
})

```

```ghost
player.onChat("foliage", function () {
    for (let index = 0; index < 8; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        for (let index = 0; index < 2; index++) {
            agent.move(FORWARD, 1)
            agent.turn(RIGHT_TURN)
        }
    }
})
``` 
