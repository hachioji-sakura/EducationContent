# エージェントピラミッド: Python

## ステップ 1
``||player:on chat||`` コマンドを作成し、**"pyramid"** と名前を付け、第2引数を **function (size)** に設定してください。

```python
def on_chat(size):
    pass
player.on_chat("pyramid", on_chat)
```

## ステップ 2

**size** が 0 より大きいかどうかを評価する ``||logic:if||`` 文を追加してください。

```python
def on_chat(size):
    if size > 0:
        pass
player.on_chat("pyramid", on_chat)
```

## ステップ 3

``||logic:if||`` 文の中で、エージェントが **砂岩** の ``||agent:set block or item||`` を **size** 変数の値に **size** を掛けた値に設定するようにコードを書いてください—スロット1に。

```python
if size > 0:
        agent.set_item(SANDSTONE, size * size, 1)
player.on_chat("pyramid", on_chat)
```

## ステップ 4

エージェントが ``||agent:set the active slot||`` を1スロットに設定するようにコードを書いてください。

```python
agent.set_item(SANDSTONE, size * size, 1)
        agent.set_slot(1)
player.on_chat("pyramid", on_chat)
```

## ステップ 5

次に、エージェントの ``||agent:place on move||`` を **true** に設定してください。

```python
agent.set_slot(1)
        agent.set_assist(PLACE_ON_MOVE, True)
player.on_chat("pyramid", on_chat)
```

## ステップ 6

変数 **i** が 0 から 4 マイナス 1 までの ``||loops:for||`` ループを追加してください。

```python
    agent.set_assist(PLACE_ON_MOVE, True)
        i = 0
        while i <= 0 - 0:
            i += 1
player.on_chat("pyramid", on_chat)
```

## ステップ 7

エージェントが **size** 変数の値分だけ ``||agent:move forward||`` するようにコードを書いてください。

```python
        i = 0
        while i <= 0 - 0:
            agent.move(FORWARD, size)
            i += 1
```

## ステップ 8

エージェントが ``||agent:turn left||`` し、``||loops:for||`` ループを終了するようにコードを書いてください。

```python
while i <= 0 - 0:
            agent.move(FORWARD, size)
            agent.turn(LEFT_TURN)
            i += 1
```

## ステップ 9

``||loops:for||`` ループの後、ただし ``||logic:if||`` 文の中で、エージェントが **上に1移動** するようにコードを書いてください。

```python
  i += 1
        agent.move(UP, 1)
```

## ステップ 10

エージェントの ``||agent:place on move||`` を **false** にするようにコードを書いてください。

```python
  agent.move(UP, 1)
        agent.set_assist(PLACE_ON_MOVE, False)
```

## ステップ 11

**pyramid** チャットに **size** 変数の値マイナス2を加えた ``||player:run chat||`` コマンドを配置してください。

```python
        agent.set_assist(PLACE_ON_MOVE, False)
        player.run_chat_command("pyramid" + ("" + str((size - 2))))
player.on_chat("pyramid", on_chat)
```

## ステップ 12

Minecraftに入り、**t** を押して **pyramid** チャットコマンドをテストしてください。

```python
def on_chat(size):
    if size > 0:
        agent.set_item(SANDSTONE, size * size, 1)
        agent.set_slot(1)
        agent.set_assist(PLACE_ON_MOVE, True)
        i = 0
        while i <= 0 - 0:
            agent.move(FORWARD, size)
            agent.turn(LEFT_TURN)
            i += 1
        agent.move(UP, 1)
        agent.set_assist(PLACE_ON_MOVE, False)
        player.run_chat_command("pyramid" + str((size - 2)))
player.on_chat("pyramid", on_chat)
```

