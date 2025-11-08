### @explicitHints true

# アクティビティ 2 - 岩石の破壊

```python
agent.destroy(FORWARD)
agent.place(RIGHT)
agent.collect_all()
agent.move(FORWARD, 5)
agent.till(BACK)
for i in range(4):
      pass
if agent.inspect(AgentInspection.BLOCK, FORWARD) == GRASS:
    pass
else: 
    pass
```

## ステップ 1
**パート 1:** エージェントが前進しながら、進路にある各**石**ブロックを破壊して収集するようなコードを書いてください。
### ~ tutorialhint
エージェント検査条件コマンドの構造:
```python
agent.inspect(AgentInspection.BLOCK, DIRECTION) == BLOCK_TYPE
```

## ステップ 2 
**パート 2:** エージェントが**草**ブロックを耕して苗木を植えるようにコードに追加してください。
### ~ tutorialhint
エージェント検査条件コマンドの構造:
```python
agent.inspect(AgentInspection.BLOCK, DIRECTION) == BLOCK_TYPE
```

```template
//# の行を正しいコードに置きかえましょう。
//以下の関数についてのコメントに置き換える                  |パート 1   
//関数1を宣言する                                         |パート 1
//エージェントに前方のブロックを破壊させる                   |パート 1
    agent.move(FORWARD, 1)
//以下の関数についてのコメントに置き換える                          |パート 2   
//関数2を宣言する                                                 |パート 2
//エージェントを前方に移動させる                                        |パート 2
//エージェントに後方を耕させる                                           |パート 2
//エージェントに後方に配置させる                                          |パート 2
//# の行を正しいコードに置きかえましょう。  
//forループを12に設定                                         |パート 1
//STONE用のエージェント検査条件を持つIf else条件文 |パート 1
//岩を除去する関数を呼び出す                           |パート 1
//GRASS用のエージェント検査条件を持つElif条件文            |パート 2            
//木を植える関数を呼び出す                                   |パート 2
//if else条件文のelse部分                           |パート 1
//エージェントを前方に移動させる                                |パート 1          
```
