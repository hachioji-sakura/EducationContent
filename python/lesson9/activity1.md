### @explicitHints true
### @hideIteration true 
# アクティビティ 1 - ゲームコントロール  

```python
agent.move(FORWARD, 5)
pos(0, 0, 0)
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
コントローラーには2つの「ボタン」があります。**青**はエージェントを左に移動させ、**赤**はエージェントを右に移動させます。赤や青のブロックの上に立ったときにエージェントが正しい方向に移動するようなコードを書いてください。

### ~ tutorialhint
条件を**True**に設定した`||loops:while||`ループは継続的に繰り返します。 

```template
//# の行を正しいコードに置きかえましょう。
//以下の関数についてのコメントに置き換える      
//関数を宣言する                                
//ブロック条件テストを持つIf条件文 (LIGHT_BLUE_CONCRETE)
//エージェントを右に移動させる
//ブロック条件テストを持つElif条件文 (RED_CONCRETE)
//エージェントを左に移動させる
//# の行を正しいコードに置きかえましょう。    
//Trueを条件とするWhileループ 
//関数を呼び出す                      
```
