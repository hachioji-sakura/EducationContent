### @explicitHints true
### @hideIteration true 
# アクティビティ 3 - 一歩ずつ

```python
blocks.place(GRASS_BLOCK, pos(0, 0, 0))
blocks.block_with_data(GRASS_BLOCK, 0)
```

## ステップ 1
**レンガブロック**（bricks）で完全な階段を作るためのコードを書いてください。3つすべての`||blocks: blockをposに置く||`コマンドで、**2番目**のパラメータの**2番目**と**3番目**の座標を変更する必要があります。また、`||blocks: blockグループのdata番のブロック||`コマンドのデータ値も更新する必要があります。各データ値は階段の方向を表すことを覚えておいてください。

### ~ tutorialhint 
壁を見て東、西、北、南の方向を確認してください。
データ値について: 
0 = W（西）  
1 = E（東）   
2 = N（北）  
3 = S（南）

```ghost
# 1段目
blocks.place(BRICKS, pos(0, 0, 1))
blocks.place(BRICKS, pos(0, 0, 2))
blocks.place(BRICKS, pos(0, 0, 3))

# 2段目
blocks.place(BRICKS, pos(0, 1, 2))
blocks.place(BRICKS, pos(0, 1, 3))

# 3段目
blocks.place(BRICKS, pos(0, 2, 3))
```