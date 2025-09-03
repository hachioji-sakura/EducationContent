### @explicitHints true
# アクティビティ 2 - スピンサイクル

```python
for i in range(2):
pass
agent.collect_all()
agent.move(FORWARD, 5)
agent.drop_all(FORWARD)
agent.turn(LEFT)

```

## ステップ 1
**パート 1:** エージェントが汚れた洗濯物を拾い、マシンに**前方**に移動し、左に**20**回回転してから、マシンから出て、汚れた洗濯物があった場所の反対側にきれいな洗濯物を置くようなコードを書いてください。

```ghost
agent.collect_all()
agent.move(FORWARD, 7)
agent.drop_all(FORWARD)
# ループ番号1                              | パート 1
for i in range(20):
    agent.turn(TurnDirection.LEFT)
# エージェントを左に20回回転させる          | パート 1 
# ループ1の終了
# エージェントにすべてを収集させる                 | パート 1          
agent.collect_all()
# エージェントを後ろに移動させる                   | パート 1
agent.move(BACK, 7)
# すべてを左にドロップさせる | パート 1
agent.drop_all(LEFT)
```

## ステップ 2
**パート 2:** 同じコードを編集して、エージェントが同じことを**3**回の洗濯に対して行うようにしてください。他のすべてのコードの前に`||loops: for||`ループを使用してこれを行ってください。

```ghost
# iとjの変数を使うこと！             | パート 2
for i in range(3):
    agent.collect_all()
    agent.move(FORWARD, 7)
    agent.drop_all(FORWARD)
    for j in range(20):
        agent.turn(TurnDirection.LEFT)        
    agent.collect_all()
    agent.move(BACK, 7)
    agent.drop_all(LEFT)
```

### ~ tutorialhint 
この場合、2つのループが同じ変数名を持つべきではないことを忘れないでください。そのため、2番目のループの名前を変更してください。
大きなコードをインデントするには、インデントしたいすべてのコードをハイライトして**tab**キーを押してください。

```template
//# の行を正しいコードに置きかえましょう。    
//ループ番号2を3に設定             | パート 2
agent.collect_all()
agent.move(FORWARD, 7)
agent.drop_all(FORWARD)
//ループ番号1                      | パート 1
//エージェントを左に20回回転させる    | パート 1 
//ループ1の終了
//エージェントにすべてを収集させる    | パート 1          
//エージェントを後ろに移動させる     | パート 1
//すべてを左にドロップさせる         | パート 1
//ループ2の終了
```
