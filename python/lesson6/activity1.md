### @explicitHints true

# アクティビティ 1 - 停止と進行

```python
loops.pause(2000)
agent.move(FORWARD, 5)
for i in range(2):
      pass
if True:
      pass
agent.detect(AgentDetection.BLOCK, FORWARD)
```

## ステップ 1
**パート 1:** エージェントが左側にブロックが**ある**時のみ移動するようなコードを書いてください。
条件に`||agent: agent detect||`コマンドを使用してください:
```python
agent.detect(AgentDetection.BLOCK, LEFT)
```

```ghost
for i in range(6):             
    if agent.detect(AgentDetection.BLOCK, LEFT):
        agent.move(FORWARD, 1)
    loops.pause(2000)
```

## ステップ 2
**パート 2:** エージェントが左側にブロックが**ない**時に移動するようにコードを編集してください。
条件の前に**not**演算子を追加してこれを行ってください。

```ghost
for i in range(7):
    if not agent.detect(AgentDetection.BLOCK, LEFT):
        agent.move(FORWARD, 1)
    loops.pause(2000)
```

## ステップ 3
**パート 3:** `||loops:pause||`コマンドの後に、最後の金ブロックに到達するためにエージェントを再び移動させてください。

```ghost
for i in range(7):
    if not agent.detect(AgentDetection.BLOCK, LEFT):
        agent.move(FORWARD, 1)
    else:
        loops.pause(100)
    loops.pause(2000)
    agent.move(FORWARD, 1)
```

### ~ tutorialhint
**1000**ミリ秒は**1**秒です。

```template
//# の行を正しいコードに置きかえましょう。    
//forループを7に設定                  |パート 1
//以下の条件にNOT演算子を追加           |パート 2 
//エージェント検出条件を持つif条件文     |パート 1
//エージェントを前方に移動させる         |パート 1
//エージェント検出条件を持つif条件文     |パート 3
loops.pause(2000)
//エージェントを前方に移動させる         |パート 3
//ループの終了
```
