### @explicitHints true

# アクティビティ 1 - 水の障壁

```python
agent.turn(LEFT_TURN)
agent.place(RIGHT)
agent.move(FORWARD, 5)
agent.detect(AgentDetection.BLOCK, FORWARD) 
while True:
      pass
```

## ステップ 1
**パート 1:** エージェントの前にレッドストーンダストがある時に前進するようなコードを書いてください。

```python
agent.detect(AgentDetection.REDSTONE, FORWARD) 
```

```ghost
while agent.detect(AgentDetection.REDSTONE, FORWARD):
    agent.move(FORWARD, 1) 
```

## ステップ 2 
**パート 2:** エージェントが移動しながら右側に2ブロックの高さの壁を配置するようにコードにシーケンスを追加してください。

### ~ tutorialhint
エージェントにブロックを与える必要はありません。既にインベントリに必要なブロックを持っています。

```ghost  
while agent.detect(AgentDetection.REDSTONE, FORWARD):
    agent.place(RIGHT)
    agent.move(UP, 1)
    agent.place(RIGHT)
    agent.move(DOWN, 1)
    agent.move(FORWARD, 1)                   
```

```template
//# の行を正しいコードに置きかえましょう。     
//エージェント検出条件を持つWhileループ            |パート 1
//エージェントに右側（RIGHT）にブロックを配置させる  |パート 2
//エージェントを上（UP）に移動させる               |パート 2
//エージェントに右側にブロックを配置させる           |パート 2
//エージェントを下（DOWN）に戻らせる               |パート 2
    agent.move(FORWARD, 1)
//whileループの終了                                
```
