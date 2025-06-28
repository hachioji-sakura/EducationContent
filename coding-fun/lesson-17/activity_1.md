### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 種を植えよう！

## ステップ 1
まず、エージェントとやり取りしてインベントリを開き、種を与えます。次に``||player:チャット時||``コマンドを作成し、``||agent:前方を耕す||``と``||agent:前方に設置||``を追加します。 

```ghost
player.onChat("plantSeed", function () {
    agent.till(FORWARD)
    agent.place(FORWARD)
})
```
