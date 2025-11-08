### @explicitHints true
 
# アクティビティ 2 - 左か右か？

```python
agent.inspect(AgentInspection.BLOCK, FORWARD)
agent.turn(LEFT_TURN)
agent.move(FORWARD, 5)
for i in range(2):
      pass
if True:
      pass
```

## ステップ 1
**パート 1:** `||logic:if else||`条件文を使用して、エージェントが看板に到達したときに左に曲がり、その後金ブロックの上に前進するようなコードを書いてください。条件として`||agent:agent inspect||`コマンドを使用し、変数**left**と比較してください。

`||agent:agent inspect||`コマンドは次のようになります:

```python
agent.inspect(AgentInspection.BLOCK, FORWARD)
```
コードで既に提供されている変数を使用してください: 
- left = BLUE_GLAZED_TERRACOTTA
- right = PINK_GLAZED_TERRACOTTA

### ~ tutorialhint 
2つの値が等しいかどうかを確認するには、**==**を使用してください。


```ghost
left = BLUE_GLAZED_TERRACOTTA
right = PINK_GLAZED_TERRACOTTA

for i in range(9):
    if agent.inspect(AgentInspection.BLOCK, FORWARD) == left:
        agent.turn(LEFT_TURN)
    else:
        agent.move(FORWARD, 1)
```

## ステップ 2
**パート 2:** エージェントが金ブロックに到達するまで両方向に曲がるようにコードを編集してください。**if**と**else**の部分の間に**elif**条件文を追加してこれを行ってください。
### ~ tutorialhint 
`||agent:agent inspect||`コマンドを条件として持つ**elif**条件文を使用し、変数**right**と比較してください。

```ghost
left = BLUE_GLAZED_TERRACOTTA
right = PINK_GLAZED_TERRACOTTA

for i in range(21):
    if agent.inspect(AgentInspection.BLOCK, FORWARD) == left:
        agent.turn(LEFT_TURN)
    elif agent.inspect(AgentInspection.BLOCK, FORWARD) == right:
        agent.turn(RIGHT_TURN)
    else:
        agent.move(FORWARD, 1)
```

```template
left = BLUE_GLAZED_TERRACOTTA
right = PINK_GLAZED_TERRACOTTA
//# の行を正しいコードに置きかえましょう。
//以下のループの値を9から21に変更          |パート 2
//forループを9に設定                     |パート 1
//エージェント検査条件を持つif else条件文   |パート 1
agent.turn(LEFT_TURN)
//エージェント検査条件を持つelif条件文      |パート 2
//エージェントを右に曲げる                 |パート 2
//if else条件文のelse部分                |パート 1
//エージェントを前方に移動させる            |パート 1
//ループの終了                           |パート 1
```
