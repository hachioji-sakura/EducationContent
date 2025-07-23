### @explicitHints true
### @hideIteration true 
# アクティビティ 1 - 動物の分類

```python
blocks.place()
mobs.spawn()
world(0, 0, 0)
```

## ステップ 1
**My_list**という名前のリストを使用して、Minecraftワールドで**左**から**右**に並んでいる動物のコードを書いてください。
すでに与えられているものの後に、さらに**4つ**の`||mobs:spawn mob at position||`コマンドを配置してください。囲いの看板の情報を使用して、これらのコマンドを完成させてください。

### ~ tutorialhint 
リストの位置は0から始まることを覚えておいてください。

```template 
location1 = world(-2, 40, -11)
location2 = world(-2, 40, -5)
location3 = world(-8, 40, -0)
location4 = world(-13, 40, -5)
location5 = world(-13, 40, -11)
//# の行を正しいコードに置きかえましょう。   

//動物のリスト

mobs.spawn(My_list[0], location1)
//リストから3番目の動物をlocation2でスポーンさせる
//リストから5番目の動物をlocation3でスポーンさせる
//リストから2番目の動物をlocation4でスポーンさせる
//リストから4番目の動物をlocation5でスポーンさせる
```
