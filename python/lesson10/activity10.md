### @explicitHints true
### @hideIteration true 

# リストにする必要がある？ 

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
リストが与えられています。各行の最初と最後からクォート（**'**）を削除してください。エージェントが立つべきブロックタイプを見つけるために、リストをアルファベット順に**ソート**し、リストから**2番目**のブロックを取得してください。正しいブロックタイプの上に立ち、ボタンを押してエージェントをそこにテレポートしてください。
プレイヤーが立つべきブロックタイプを見つけるために、リストを**逆順**にし、リストの**4番目**のブロックを**pop**してください。
リストから**6番目**のブロックを取得し、そのブロックの上に立ってください。

```template
'block_list = ["DIAMOND", "ICE", "EMERALD", "STONE", "WOOD", "GOLD", "QUARTZ"]'
```