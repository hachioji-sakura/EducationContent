### @explicitHints true
### @hideIteration true 
# アクティビティ 2 - 防火帯

```python
agent.turn(LEFT_TURN)
agent.place(RIGHT)
agent.move(FORWARD, 5)
agent.detect(AgentDetection.BLOCK, FORWARD) 
while True:
      pass
```

## ステップ 1
エージェントの前にレッドストーンダストがある時に前進するようなコードを書いてください。
前進中にエージェントは左側に1ブロックの高さの壁を作る必要があります。
地形の高さの変化に遭遇した時、エージェントは上に移動して壁を継続する必要があります。

```template
//# の行を正しいコードに置きかえましょう。
//エージェント検出レッドストーン条件を持つWhileループ1 
//エージェント検出ブロック条件を持つWhileループ2 
agent.place(LEFT)
//エージェントを上に移動させる                            
//エージェントに左側にブロックを配置させる         
//エージェントを前方に移動させる
//whileループ2の終了
//エージェントに左側にブロックを配置させる         
//エージェントを前方に移動させる
//whileループ1の終了                         
```