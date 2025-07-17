### @explicitHints true

# Activity 3 - Are my calculations off?

```python
player.say("hi")
item +=1
```

## ステップ 1
テレビモニター1を見て、**cost**という新しい変数を作成して表示されている合計を計算してください。コードを実行してチャットに総コストを表示してください。
その合計に対応するボタンを押してください。

## ステップ 2
テレビモニター2を見てください。新しい作物**pumpkin**を追加する必要があります。**pumpkin**という変数を作成し、その値を変数**berries**と**apple**の差として設定してください。新しい変数**pumpkin**を変数**cost**に追加してください。その後、
コードを実行して正しいボタンを押してください。

## ステップ 3 
最後のテレビモニターを見てください。作物**apple**と**melon**の値が変更されました。**Apple**は価格が**2**上がり、
**melon**は価格が**3**下がりました。**+=**と**-=**演算子を使用してコードでこの変更を反映してください。

```template
apple = 10
melon = 15
berries = 20
potato = 2
//# の行を正しいコードに置きかえましょう。
//pumpkin 変数      | ステップ 2
//appleの変更       | ステップ 3
//melonの変更       | ステップ 3
//cost変数          | ステップ 1
player.say(cost)
``` 

```ghost
apple = 10
melon = 15
berries = 20
potato = 2
# Replace the lines below with your code #
pumpkin = berries - apple
apple += 2                          
melon -= 3
cost = apple + melon + berries * 2 + potato + pumpkin
player.say(cost)
```