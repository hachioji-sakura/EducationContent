### @explicitHints true

# アクティビティ 3 - 家の再建

```python
agent.turn(LEFT_TURN)
agent.place(RIGHT)
agent.move(FORWARD, 5)
agent.detect(AgentDetection.BLOCK, FORWARD) 
while True:
      pass
```

## ステップ 1
**パート 1:** エージェントがレッドストーンダストのガイドラインに従い、左側にブロックを配置して小さな家の基礎を作るようなコードを書いてください。
**2つ**の`||loops:while||`ループを使用してください。1つは直線部分用、もう1つは角を曲がる部分用です。

```python
agent.detect(AgentDetection.REDSTONE, FORWARD) 
```

```ghost
while agent.detect(AgentDetection.REDSTONE, FORWARD):
    agent.place(LEFT)
    agent.move(FORWARD, 1)
    while agent.detect(AgentDetection.REDSTONE, LEFT):
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
```

## ステップ 2 
**パート 2:** エージェントがより大きな家の基礎を建設するようにコードに追加してください。内角用も建設できるように追加の`||loops:while||`ループを書いてください。
### ~ tutorialhint 
内角用のコードを書く時、エージェントがブロックを配置するために輪郭を1ブロック超えて移動し、その後戻る部分を含める必要があります。

```ghost
while agent.detect(AgentDetection.REDSTONE, FORWARD):
    agent.place(LEFT)
    agent.move(FORWARD, 1)
    while agent.detect(AgentDetection.REDSTONE, LEFT):
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
    while agent.detect(AgentDetection.REDSTONE, RIGHT) and not agent.detect(AgentDetection.REDSTONE, FORWARD):
    // このループの中では agent.move(FORWARD)を行うため、一歩前に進んだ時に「右にレッドストーンがある」と検知されて右に曲がってしまう。このエラーを回避するために、「and not agent.detect(AgentDetection.REDSTONE, FORWARD)」を追加している。
        agent.place(LEFT)
        agent.move(FORWARD, 1)
        agent.place(LEFT)
        agent.move(BACK, 1)
        agent.turn(RIGHT_TURN)           
```

```template
//# の行を正しいコードに置きかえましょう。    
//エージェント検出条件を持つWhileループ1      |パート 1
//エージェントに左側（LEFT）にブロックを配置   |パート 1       
//エージェントを前方（FORWARD）に移動        |パート 1 
//エージェント検出条件を持つWhileループ2      |パート 1
agent.turn(LEFT_TURN)
//エージェントを前方に移動させる              |パート 1
//whileループ2の終了
//エージェント検出条件を持つWhileループ3       |パート 2
//エージェントに左側にブロックを配置させる      |パート 2        
//エージェントを前方に移動させる               |パート 2
//エージェントに左側にブロックを配置させる       |パート 2        
//エージェントを後ろ（BACK）に移動させる        |パート 2
//エージェントを右（RIGHT）に曲げる            |パート 2                 
//whileループ3の終了
//whileループ1の終了                        
```
