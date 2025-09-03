### @explicitHints true
# アクティビティ 1 - 重すぎる！

```python
for i in range(2):
pass
agent.collect_all()
agent.move(FORWARD, 5)
agent.place(FORWARD)
```

## ステップ 1
**パート 1:** エージェントが箱を拾い、**6**ブロック**前方**に移動してから**前方**に置くようなコードを書いてください。

```ghost
agent.collect_all()
agent.move(FORWARD, 6)
agent.place(FORWARD)
```

## ステップ 2
**パート 2:** 同じコードを編集して、エージェントが出発点に戻るようにしてください。同じことを**4**回行う必要があります。最初に`||loops: for||`ループを使用してください。
箱は自動的に積み重ねられます。
### ~ tutorialhint 
キーボードの**tab**キーを使用して、ループの後のすべてをインデントすることを忘れないでください。

```ghost
for i in range(4):
    agent.collect_all()
    agent.move(FORWARD, 6)
    agent.place(FORWARD)
    agent.move(BACK, 6)
```