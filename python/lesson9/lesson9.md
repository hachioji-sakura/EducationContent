### @explicitHints true
# エージェントインベーダー  

```python
pos(0, 0, 0)
mobs.spawn(FIREWORKS_ROCKET, agent.get_position())
blocks.place()
blocks.test_for_block(GRASS, pos(0, 0, 0))
positions.add(pos(0, 0, 0), pos(0, 0, 0))
pos(0, 0, 0)
loops.pause(100)
agent.move(FORWARD, 5)
agent.get_position()
gameplay.title(mobs.target(NEAREST_PLAYER), "Congratulations!", "You won!")
mobs.target(NEAREST_PLAYER)
player.say("HI")
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
**アクティビティ 1 - ゲームコントロール：**
コントローラーには2つの「ボタン」があり、青はエージェントを左に移動させ、赤はエージェントを右に移動させます。赤や青のブロックの上に立ったときにエージェントが正しい方向に移動するようなコードを書いてください。以下のtest for blockコマンドを使用して、ブロックが特定の位置にあるかどうかを確認してください：
```python
blocks.test_for_block(BLOCK_NAME, pos(0, 0, 0))
```

### ~ tutorialhint
条件を**True**に設定した`||loops:while||`ループは継続的に繰り返します。コーディングウィンドウで事前に与えられたコードを削除**しない**でください。

## ステップ 2
**アクティビティ 2 - 発射システム -**
**パート 1:** エージェントが上にある金ブロックを撃つようにする別の関数を書いてください。
**FIREWORKS_ROCKET**と一緒に`||mobs: mob spawn||`コマンドを使用して撃ってください。撃たれた各金ブロックは**AIR**ブロックで置き換えて消えるようにする必要があります。
`||agent: agent position||`コマンドを使用してエージェントの位置を取得してください。
**AIR**ブロックの位置を取得するために、`||agent: agent position||`コマンドを含むadd positionsコマンドを使用してください。
2つのコマンドを組み合わせると次のようになります：
```python 
positions.add(agent.get_position(), pos(0, 0, 0))
```
## ステップ 3
**パート 2:** 追加の`||logic: elif||`条件文を使用して、エージェントが2列目の金ブロックを撃つようにコードに追加してください。 

## ステップ 4
**アクティビティ 3 - スコアシステム：**
コードで`||variables:score||`という名前の変数が与えられています。エージェントが金ブロックを撃つたびに、この変数に**1**を追加してください。
`||variables:score||`が**15**以下のときのみループするように、whileループの条件を編集してください。
`||gameplay:show title||`コマンドを使用して、ゲームの開始と終了に2つのスプラッシュスクリーンを追加してください。以下のコマンドを使用して`||variable:score||`変数をグローバルとして宣言してください：
```
global score 
```

### ~ tutorialhint
**<=**は**以下**を意味します。


```template
//# の行を正しいコードに置きかえましょう。
//関数2を宣言する                                                          |アクト. 2 パート 1
//スコア変数をグローバルとして宣言する                                                           |アクト. 3      
//ブロック条件テスト、エージェント位置 + 2を持つIf条件文                     |アクト. 2 パート 1
//エージェントの位置で花火ロケットをスポーンする                                    |アクト. 2 パート 1
//100ms間一時停止                                                             |アクト. 2 パート 1
//エージェント位置 + 2にAIRブロックを配置する                                            |アクト. 2 パート 1
//変数scoreに1を追加する                                                                |アクト. 3
//ブロック条件テスト、エージェント位置 + 3を持つElif条件文                   |アクト. 2 パート 2
//エージェントの位置で花火ロケットをスポーンする                                    |アクト. 2 パート 2
//100ms間一時停止                                                             |アクト. 2 パート 2
//エージェント位置 + 3にAIRブロックを配置する                                            |アクト. 2 パート 2
//変数scoreに1を追加する                                                                |アクト. 3
//以下の関数についてのコメントに置き換える                           |アクト. 1      
//関数を宣言する                                                    |アクト. 1
//ブロック条件テスト (LIGHT_BLUE_CONCRETE)を持つIf条件文  |アクト. 1
//エージェントを右に移動させる                                           |アクト. 1
//ブロック条件テスト (RED_CONCRETE)を持つElif条件文       |アクト. 1
//エージェントを左に移動させる                                            |アクト. 1
//# の行を正しいコードに置きかえましょう。  
score = 0
//gameplay titleコマンドを使用して開始スプラッシュスクリーンを追加                                 |アクト. 3
//scoreが15以下の時のみループするようにwhileループを変更                                         |アクト. 3
//Trueを条件とするWhileループ                                   |アクト. 1
//関数を呼び出す                                                       |アクト. 1
//関数2を呼び出す                                                             |アクト. 2 パート 1
//gameplay titleコマンドを使用して終了スプラッシュスクリーンを追加                                   |アクト. 3
//エージェントの位置に雷を発生させる                                                      |アクト. 3  
if score > 15
player.execute("scoreboard players set @p score 15")
```
