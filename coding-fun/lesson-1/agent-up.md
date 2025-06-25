### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムして金のプレートまで上に移動させよう！

## ステップ 1
``||player:チャット時||``と``||agent:エージェント移動||``コマンドを使用して、エージェントが金のプレートに向かって移動するようにプログラムします。エージェントを**上**に移動するようにプログラムできます。完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftに移動してゲーム内でコードを実行してください。



```ghost
player.onChat("up", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})

```  
