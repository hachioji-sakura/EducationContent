# 木の伐採: Python

## ステップ 1

``||player:on chat||`` コマンドを作成し、**"tp"** と名前を付けてください。

```python
def on_chat():
    pass
player.on_chat("tp", on_chat)
```

## ステップ 2

``||player:chat||`` コマンドの中で、エージェントがプレイヤーに ``||agent:teleport||`` するようにコードを書いてください。

```python
def on_chat2():
    agent.teleport_to_player()
player.on_chat("tp", on_chat)
```

## ステップ 3

別の ``||player:chat||`` コマンドを作成し、**"chop"** と名前を付けてください。

```python
def on_chat3():
    pass
player.on_chat("chop", on_chat)
```

## ステップ 4

新しい ``||variable:variable||`` を作成し、**height** と名前を付け、**0** に設定してください。

```python
height = 0
def on_chat():
    agent.turn(LEFT_TURN)
player.on_chat("lt", on_chat)
def on_chat2():
    agent.teleport_to_player()
player.on_chat("tp", on_chat2)
def on_chat3():
    height = 0
player.on_chat("chop", on_chat3)
```

## ステップ 5

**chop** ``||player:on chat||`` コマンドの中で、**height** 変数の直下に、**エージェントが前方にブロックを検出している間** から始まる ``||loops:while||`` ループを作成してください。

```python
def on_chat3():
    height = 0
    while agent.detect(AgentDetection.BLOCK, FORWARD):
        pass
player.on_chat("chop", on_chat3)
```

## ステップ 6

``||loops:while||`` ループに、**height** ``||variable:variable||`` を **height プラス 1** の値に変更する処理を追加してください。

```python
    while agent.detect(AgentDetection.BLOCK, FORWARD):
        height += 1
player.on_chat("chop", on_chat3)
```

## ステップ 7

``||loops:while||`` ループの中で、変数 **height** の変更の下に、エージェントが **上方向を破壊** するようにコードを書いてください。

また、**エージェントが上に1移動** する行も追加してください。

```python
        height += 1
        agent.destroy(UP)
        agent.move(UP, 1)
player.on_chat("chop", on_chat3)
```

## ステップ 8

``||loops:while||`` ループの後に ``||loops:for||`` ループを追加してください。``||loops:repeat||`` ループの **times** 引数に **height** 変数を挿入してください。

```python
    for index in range(height):
```

## ステップ 9

``||loops:for||`` ループの中に、**エージェントが下に1移動** と **エージェントが前方を破壊** の行を追加してください。

```python
    for index in range(height):
        agent.move(DOWN, 1)
        agent.destroy(FORWARD)
    player.on_chat("chop", on_chat3)
```

## ステップ 10

``||loops:for||`` ループの後に、エージェントが ``||agent:collect all||`` するようにコードを書いてください。

```python
    for index in range(height):
        agent.move(DOWN, 1)
        agent.destroy(FORWARD)
    agent.collect_all()
player.on_chat("chop", on_chat3)
```

## ステップ 11

Minecraftに入り、**t** を入力して **tp** と **chop** チャットコマンドをテストしてください。 

```python
def on_chat(): 

    agent.set_item(CARROTS, 64, 1) 
