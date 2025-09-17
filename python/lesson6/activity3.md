### @explicitHints true
### @hideIteration true 
# アクティビティ 3 - 通り抜ける

```python
agent.detect(AgentDetection.BLOCK, FORWARD) 
agent.turn(LEFT_TURN)
agent.move(FORWARD, 5)
for i in range(2):
      pass
if True:
      pass
```

## ステップ 1
エージェントがコースを通り抜ける際に、ランダムに配置されたブロックを検出して回避するようなコードを書いてください。これを行うには、間に**elif**条件文を持つ`||logic:if else||`条件文を使用してください。**if**条件には、間に**and not**演算子を持つ2つの`||agent:agent detect||`コマンドを使用してください。**elif**条件には、間に**and**演算子を持つ2つの`||agent:agent detect||`コマンドを使用してください。**and not**演算子を持つ2つの条件の例:
```python
agent.detect(AgentDetection.BLOCK, DIRECTION) and not agent.detect(AgentDetection.BLOCK, DIRECTION)
```

### ~ tutorialhint 
複数の条件を一緒に使用する場合、**and**または**and not**を使用して複数の状態をチェックできます。

```template
//# の行を正しいコードに置きかえましょう。    
//forループを23に設定                                            
//and not演算子で区切られた2つのエージェント検出コマンドを持つif else条件文
agent.move(LEFT, 1)                              
//and演算子で区切られた2つのエージェント検出コマンドを持つelif条件文
agent.move(RIGHT, 2)
//else if条件文のelse部分             
agent.move(FORWARD, 1)                                   
//ループの終了                                       
```
