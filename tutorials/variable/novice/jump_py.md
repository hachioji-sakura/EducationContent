# メガジャンプ: Python

## ステップ 1
**"jump"** という名前の ``||player:on chat||`` コマンドを追加してください。

```python
def on_chat():
    pass
player.on_chat("jump", on_chat)
```

## ステップ 2

``||player:chat||`` コマンドの中に、プレイヤーを位置 **(0,100,0)** （現在の位置より100ブロック高い位置）に ``||player:teleport||`` するコードを追加してください。

```python
def on_chat(): 
    player.teleport(pos(0, 100, 0)) 
player.on_chat("jump", on_chat) 
```

## ステップ 3

Minecraftでチャットに jump と入力して試してみてください。


## ステップ 4

"jump" チャットコマンドに **num1** という名前の ``||variables: variable||`` を追加してください。

```python
def on_chat(num1): 
    player.teleport(pos(0, 100, 0)) 
player.on_chat("jump", on_chat) 
```

## ステップ 5

``||player:teleport||`` にある **100** を ``||variables:variable||`` **num1** に変更してください。

```python
def on_chat(num1):
    player.teleport(pos(0, num1, 0))
player.on_chat("jump", on_chat) 
```

## ステップ 6

Minecraftでチャットに jump と任意の数字を入力して試してみてください。（例：jump 50、または jump 100） 

```python
def on_chat(num1):
    player.teleport(pos(0, 100, 0))
player.on_chat("jump", on_chat)
```

