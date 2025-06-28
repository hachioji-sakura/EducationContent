### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 資源を採掘しよう！

## ステップ 1
エージェントは**金鉱石**と**鉄鉱石**ブロックを採掘する必要があります。エージェントが様々な方向（例：**前進**、**後退**、**右**）に移動するようにプログラムする、複数の``||player:チャット時||``コマンドを作成してみてください。エージェントをどこまで移動させたいかを指定する代わりに、変数を使用できます。ゲーム内チャットでコマンドを入力する際、エージェントを**5歩前進**させたい場合は**forward 5**のように**forward**と**数字**を入力します。この方法で、コードを変更することなく、エージェントが移動する必要のある歩数をその場で変更できます。 

### ~ tutorialHint
エージェントに鉱物を採掘させるため、``||agent:破壊||``と``||agent:収集||``ブロックを追加することを忘れないでください。 

```template
player.onChat("forward", function (num1) {
    agent.move(FORWARD, num1)
})
```
```ghost
player.onChat("right", function (num1) {
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("back", function (num1) {
    agent.turn(RIGHT_TURN)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("left", function (num1) {
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("collect", function () {
    agent.destroy(DOWN)
    agent.collectAll()
})
```


