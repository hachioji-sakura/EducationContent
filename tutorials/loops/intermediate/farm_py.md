# Farm: Python

## 農場を作ろう @showdialog
このチュートリアルでは、2重のfor文を使う練習をします。
農場を作るためのコードを書いてみましょう。

## ステップ 1
``||player:チャットコマンドを実行した時||`` のイベントを作成して、チャットコマンドに **tp** と入力された場合のコードを作成します。
そして、``||agent:エージェントをプレイヤーの位置にテレポートする||`` をコードを関数の中に追加します。

```python
def on_chat():
    agent.teleport_to_player()
player.on_chat("tp", on_chat)
```

## Step 2
``||player:チャットコマンドを実行した時||`` のイベントを追加して、名前を **farm** (ファーム) にします。

```python
def on_chat():
    pass
player.on_chat("farm", on_chat)
```

## Step 3
``||agent:エージェントにアイテムを持たせる||`` コードを使用して、**64** 個の **キャロット** (CARROTS) をスロット **1** に設定します。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
player.on_chat("farm", on_chat)
```

## Step 4
``||loops:for||`` ループを使用して、**2** 回繰り返すコードを書いてください。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        pass
player.on_chat("farm", on_chat)
```

## Step 5
``||loops:for||`` ループの中で、``||agent:エージェントを移動させる||`` コードを使用して、後ろ（**BACK**）へ **7** ブロック、移動します。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        agent.move(BACK, 7)
player.on_chat("farm", on_chat)
```

## Step 6
``||agent:エージェントを移動させる||`` コードを使用して、右（**RIGHT**）へ **4** ブロック移動します。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        agent.move(BACK, 7)
        agent.move(RIGHT, 4)
player.on_chat("farm", on_chat)
```

## Step 7
``||loops:for||`` ループを使用して、**7** 回繰り返すコードを追加してください。最初の ``||loops:for||`` ループの中かつ、``||agent:エージェントを移動させる||`` コードの前に追加します。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        for index2 in range(7):
            pass
        agent.move(BACK, 7)
        agent.move(RIGHT, 4)
player.on_chat("farm", on_chat)
```

## Step 8
``||loops:for||`` ループの中で、``||agent:エージェントに耕させる||`` コードを使用して、前（**FORWARD**）へ耕します。 

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        for index2 in range(7):
            agent.till(FORWARD)
        agent.move(BACK, 7)
        agent.move(RIGHT, 4)
player.on_chat("farm", on_chat)
```

## Step 9
``||agent:エージェントを移動させる||`` コードを使用して、前（**FORWARD**）へ **1** ブロック移動します。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        for index2 in range(7):
            agent.till(FORWARD)
            agent.move(FORWARD, 1)
        agent.move(BACK, 7)
        agent.move(RIGHT, 4)
player.on_chat("farm", on_chat)
```

## Step 10
``||agent:エージェントを移動させる||`` コードを使用して、下（**DOWN**）へ **1** ブロック移動します。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(2):
        for index2 in range(7):
            agent.till(FORWARD)
            agent.move(FORWARD, 1)
            agent.place(DOWN)
        agent.move(BACK, 7)
        agent.move(RIGHT, 4)
player.on_chat("farm", on_chat)
```

## Step 11
緑の実行ボタンを押し、Minecraftでコードをテストしてください。

```python
def on_chat():
    agent.set_item(CARROTS, 64, 1)
    for index in range(3):
        for index2 in range(5):
            agent.till(FORWARD)
            agent.move(FORWARD, 1)
            agent.place(DOWN)
        agent.move(BACK, 5)
        agent.move(RIGHT, 2)
player.on_chat("farm", on_chat)
```

