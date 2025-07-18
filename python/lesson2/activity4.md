### @explicitHints true
### @hideIteration true 
# アクティビティ 4 - 向こう側へ

```python
blocks.place(GRASS_BLOCK, pos(0, 0, 0))
```

## ステップ 1
向こう側へ渡るために、5つの**オークの板ブロック**で作られた床の一列を作るコードを書いてください。`||blocks: blockをposに置く||`コマンドで**2番目**のパラメータの**1番目**と**2番目**の座標を変更する必要があります。床と同じ高さで橋を建設することに注意してください。

- オークの板 = oak planks

### ~ tutorialhint 
座標に負の数を使用してみてください。

```ghost
blocks.place(PLANKS_OAK, pos(-1, -1, 0))
blocks.place(PLANKS_OAK, pos(-2, -1, 0))
blocks.place(PLANKS_OAK, pos(-3, -1, 0))
blocks.place(PLANKS_OAK, pos(-4, -1, 0))
blocks.place(PLANKS_OAK, pos(-5, -1, 0))
```