### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# エージェントをプログラムして金のプレートまで移動させよう！

## ステップ 1
``||player:チャット時||``コマンドを選択し、名前を**run**から**1**に変更します。``||agent:エージェント前進||``ブロックを選択し、``||player:チャット時||``コマンドの内部にドラッグします。エージェントが金のプレートに到達できるように、エージェントが移動する**歩数**を**3**に変更します。完了したら、**再生**ボタンを押してコードをコンパイルし、Minecraftに移動して**t**を押し、**1**と入力します。

#### ~ tutorialhint 
``||agent:エージェント移動||``ブロック内の数字を変更することで、エージェントが移動する歩数を変更できます。また、``||agent:エージェント回転||``ブロックを使用してエージェントを左または右に回転させることもできます。



```ghost
player.onChat("1", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})

``` 
