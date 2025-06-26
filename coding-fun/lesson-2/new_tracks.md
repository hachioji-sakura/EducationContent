### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムしてカメの足跡に沿って移動させよう！

## ステップ 1
``||agent:エージェントを移動させる||``ブロックを使用して、エージェントをカメの足跡に沿って移動させます。

#### ~ tutorialhint 
``||loops:くりかえし||``ブロックを使用してコードをより効率的にしてみてください。

## ステップ 2
完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftでコードを実行することを忘れないでください。

```blocks
player.onChat("run", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
``` 

