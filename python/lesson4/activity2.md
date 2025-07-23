### @explicitHints true

# アクティビティ 2 - 食事の必要条件

```python
blocks.place()
```

## ステップ 1
**最初**の犬に、事前定義されたリストに既にあるすべてのものを与えるために、最初の**4つ**の`||blocks:place block at position||`コマンドの値を変更してください。リストの項目を順番に1つずつ配置するようにしてください。その後、チェストから犬1番に餌を与えてください。

### ~ tutorialhint 
ホットバーからアイテムをドロップするには、キーボードの[**Q**]キーを押してください。

## ステップ 2
**2番目**の犬に、追加のビタミンが加わったリストのすべてのものを与えてください。
**append**メソッドを使用して変数**Vitamins**をリストの最後に追加してください。
その後、最後の`||blocks: place block at position||`コマンドの値を変更して、マシンにビタミンを配置し、犬2番に餌を与えてください。

## ステップ 3
**3番目**の犬に、リストのすべてのものから**beef**を除いたものを与えてください。
**pop**メソッドを使用して変数**Beef**をリストから削除してください。
その後、犬3番に餌を与えてください。

### ~ tutorialhint 
**pop**メソッドでは、名前ではなくリストの位置の値を使用する必要があります。

```template
Bone = world(-21, 45, -31)
Beef = world(-21, 45, -29)
Chicken = world(-21, 45, -27)
Biscuit = world(-21, 45, -25)
Vitamins = world(-21, 45, -23)
//# の行を正しいコードに置きかえましょう。   
Dog_Food=[Bone, Beef, Chicken, Biscuit]
//appendメソッドを使用してリストに変数Vitaminsを追加する | ステップ 2
//popメソッドを使用して変数Beefを削除する                  | ステップ 3

blocks.place(REDSTONE_BLOCK, Dog_Food[0]) 
//下のリストの数値を変更する         | ステップ 1
blocks.place(REDSTONE_BLOCK, Dog_Food[0])
//下のリストの数値を変更する         | ステップ 1
blocks.place(REDSTONE_BLOCK, Dog_Food[0]) 
//下のリストの数値を変更する         | ステップ 1
blocks.place(REDSTONE_BLOCK, Dog_Food[0])   
//下のリストの数値を変更する                  | ステップ 2
blocks.place(REDSTONE_BLOCK, Dog_Food[0]) 
```