### @explicitHints true
# アクティビティ 3 - 片付け

```python
for i in range(2):
pass
agent.collect_all()
agent.move(FORWARD, 5)
agent.drop_all(FORWARD)
```

## ステップ 1
**パート 1:** エージェントが小さなカーペットのすべてのブロックを通り、汚れを拾うようなコードを書いてください。
### ~ tutorialhint 
この場合、2つのループが同じ変数名を持つべきではないことを忘れないでください。

```ghost
# Agentの向きによって、コメントの指示と方向を変える必要があることに注意
for i in range(7):
    agent.collect_all()
    agent.move(BACK, 1)
# ループ1の終了
agent.move(LEFT, 1)
# ループ番号2                        | パート 1
for i in range(7):
    agent.collect_all()
    agent.move(FORWARD, 1)
# エージェントにすべてを収集させる           | パート 1  
# エージェントを後ろに移動させる             | パート 1  
```

## ステップ 2
**パート 2:** 同じコードを編集して、エージェントが大きなカーペットに対して同じことを行うようにしてください。`||loops:for||`ループを使用してコードを**3**回繰り返してこれを行ってください。最後に、エージェントにすべての汚れを**右**のゴミ箱にドロップさせてみてください。
### ~ tutorialhint 
コードで二重インデントを使用する必要があることを覚えておいてください。

```ghost
for j in range(3):
    for i in range(7):
        agent.collect_all()
        agent.move(BACK, 1)
    agent.move(LEFT, 1)
    for i in range(7):
        agent.collect_all()
        agent.move(FORWARD, 1)
    agent.move(LEFT, 1)
agent.move(LEFT, 1)
agent.drop_all(LEFT)
```

```template
//# の行を正しいコードに置きかえましょう。    
//ループ番号3                                 | パート 2
//ループ番号1                        | パート 1
agent.collect_all()
agent.move(FORWARD, 1)
//ループ1の終了
agent.move(RIGHT, 1)
//ループ番号2                        | パート 1
//エージェントにすべてを収集させる           | パート 1  
//エージェントを後ろに移動させる             | パート 1  
//ループ2の終了
//エージェントを右に移動させる                     | パート 2
//ループ3の終了  
//エージェントにすべてを右にドロップさせる          | パート 2  
```
