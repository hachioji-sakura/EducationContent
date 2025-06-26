### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムしてカメの足跡に沿って移動させよう！

## ステップ 1
``||agent:エージェントを移動させる||``ブロックを使用して、エージェントをカメの足跡に沿ってゲートまで移動させます。完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftでコードを実行することを忘れないでください。 

```ghost
player.onChat("tracks", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
``` 
