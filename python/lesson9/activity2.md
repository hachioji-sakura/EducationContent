### @explicitHints true
### @hideIteration true 
# 目くらましい光 

```python
agent.move(FORWARD, 5)
pos(0, 0, 0)
player.say("Finished")
agent.place(LEFT)
agent.inspect(AgentInspection.BLOCK, DOWN) 
agent.turn(RIGHT_TURN)
agent.destroy(BACK)
agent.drop_all(FORWARD)
agent.collect_all()
loops.pause(500)
for i in range(10):
    pass
if True: 
    pass
else: 
    pass
elif:
    pass
while True:
    pass
```

## ステップ 1
エージェントが歩道を前進しながら、レッドストーンブロックの上にレッドストーンランプを配置するようにしてください。

### ~ tutorialhint
エージェントは既に必要なすべてのブロックをインベントリに持っています。

