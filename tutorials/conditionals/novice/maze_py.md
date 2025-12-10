# エージェント迷路: Python


## ステップ 1

エージェントが前方にブロックを検出するかどうかを評価する ``||logic: if then||`` 文を作成してください。**true** と評価された場合は、左に回転します。

```python
if agent.detect(AgentDetection.BLOCK, FORWARD):
    agent.turn(LEFT_TURN)
```

## ステップ 2

``||logic: if||`` 文に ``||logic: else||`` を追加し、``||agent:agent move||`` **前方に1** コマンドの指示を含めてください。

**注意:** 完全な文は ``||logic: if-else||`` 文になります。

```python
        agent.turn(LEFT_TURN)
    else:
        agent.move(FORWARD, 1)
```

## ステップ 3

``||logic: if-else||`` 文を ``||loops: forever||`` ループ内に配置してください。これにより、これらのステップは停止するまで継続されます。

```python
def on_forever():
    if agent.detect(AgentDetection.BLOCK, FORWARD):
        agent.turn(LEFT_TURN)
    else:
        agent.move(FORWARD, 1)
loops.forever(on_forever)
```
## ステップ 5
**Play** ボタンを押して、Minecraftでコードを試してみてください。 

```ghost
agent.teleportToPlayer()
```
```python
def on_forever():
    if agent.detect(AgentDetection.BLOCK, FORWARD):
        agent.turn(LEFT_TURN)
    else:
        agent.move(FORWARD, 1)
loops.forever(on_forever)
```
