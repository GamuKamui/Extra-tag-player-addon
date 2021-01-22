## コマンドの例
### ※このコマンドの例の一部には↓のコマンドを使っておかないと動かないやつもあります
### /scoreboard objectives add haveitem dummy haveitem
### `反復`と書いていたら反復コマンドブロックで常時ONにしてください  
### `チェーン`と書いていたら無条件チェーンコマンドブロックで一行上のコマブロと接続してください  
  
  
1. スニークしているプレイヤーに耐性Ⅱをつける。  
```
反復 /effect @a[tag=sneaking] resistance 1 1
```
  
2. 走ると死ぬコマンド  
```
反復 /kill @a[tag=sprinting]  
```
  
3. ダメージを受けると目の前に雷を落とすコマンド  
```
反復 /execute @a[tag=damage] ~~~ summon lightning_bolt ^^^4  
チェーン /tag @a[tag=damage] remove damage  
```
  
4. ヘルメットが装備から外れるとtitleを出すコマンド  
```
反復 /title @a[tag=!helmet] title ヘルメットがなくなった！  
チェーン /tag @a[tag=!helmet] add helmet  
```
  
5. ハニーボトルを飲もうとすると爆発するコマンド  
```
反復 /execute @a[tag=using,scores={haveitem=582}] ~~~ summon ender_crystal ~~~ minecraft:crystal_explode  
チェーン /tag @a[tag=!using] add using  
```  
  
6. 体力が満タンのときに剣で攻撃すると目の前に爆発寸前のクリーパーを召喚するコマンド  
```
反復 /execute @a[tag=max_health,tag=attack,tag=sword] ~~~ /summon creeper ^^^6 minecraft:start_exploding  
チェーン /tag @a[tag=attack] remove attack  
```  
