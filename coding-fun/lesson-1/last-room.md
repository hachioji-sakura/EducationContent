### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムして金のプレートまで上に移動させよう！

## ステップ 1
エージェントが金のプレートに到達するようにプログラムします。あなたはあなたの金のプレートに留まり、エージェントは別のプレートに留まる必要があります。完了したら、**再生**ボタンを押してコードをコンパイルします。Minecraftに移動してコードを実行してください。


```ghost
player.onChat("last", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```  
