# ループ: Python

## for文（初級） @showdialog

for文を使って、くり返すコードを書く練習をしましょう。

アイテムを使ったらたくさんのモブが出現するコードを書いてみましょう。


## ステップ 1
``||player:アイテムが使用された時||`` のコードを使用して、アイテムを**骨**（BONE） に設定してください。

```python
def item_interacted_bone():
    pass
player.on_item_interacted(BONE, item_interacted_bone)
```

## ステップ 2
``||player: アイテムが使用された時||`` のイベントの関数内に、 ``||loops:for||`` ループを使用して**6** 回繰り返えすコードを書いてください。

```python
def item_interacted_bone():
    for index in range(6):
        pass
player.on_item_interacted(BONE, item_interacted_bone)
```

## ステップ 3
``||loops:for||`` ループの中で、位置(0,0,0) に **ゾンビホース** (ZOMBIE_HORSE) をスポーンしてください。

```python
def item_interacted_bone():
    for index in range(6):
        mobs.spawn(ZOMBIE_HORSE, pos(0, 0, 0))
player.on_item_interacted(BONE, item_interacted_bone)
```

## ステップ 4
別の``||loops:for||`` ループを追加して、今度は **4** 回繰り返すコードを書いてください。

```python
def item_interacted_bone():
    for index in range(6):
        mobs.spawn(ZOMBIE_HORSE, pos(0, 0, 0))
    for index2 in range(4):
        pass
player.on_item_interacted(BONE, item_interacted_bone)
```

## ステップ 5
``||loops:for||`` ループの中で、位置(0,0,0) に **スケルトンホース** (SKELETON_HORSE) をスポーンしてください。  

```python
def item_interacted_bone():
    for index in range(6):
        mobs.spawn(ZOMBIE_HORSE, pos(0, 0, 0))
    for index2 in range(4):
        mobs.spawn(SKELETON_HORSE, pos(0, 0, 0))
player.on_item_interacted(BONE, item_interacted_bone)
```

## ステップ 6
緑の実行ボタンを押し、Minecraftでコードをテストしてください。

```python
def item_interacted_bone():
    for index in range(6):
        mobs.spawn(ZOMBIE_HORSE, pos(0, 0, 0))
    for index2 in range(4):
        mobs.spawn(SKELETON_HORSE, pos(0, 0, 0))
player.on_item_interacted(BONE, item_interacted_bone)
```

