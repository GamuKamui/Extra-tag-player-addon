# Extra-tag-player-addon
tagコマンドによりプレイヤーでいろんなことができるようになるアドオンです。  
・・・とかいいつつtagを全く使わない要素も追加する予定です

### ⚠まだ開発段階です

## **できること**
大まかに言うと、  
特定のtagをつけるとプレイヤーに影響を与える、  
特定のアクションをするとtagがつく、  
の２つです。特に後者はワールド開発者にとっては便利なのではないでしょうか。

## 使い方  
例  
`/tag @p add nonametag` 近くにいたプレイヤーのネームタグを見えなくします。  
`/effect @a[tag=sneaking] resistance 20 1` スニークしているプレイヤーに20秒間、耐性Ⅱをつける。  
  
  
## tag説明 
### １，特定のtagをつけるとプレイヤーに影響を与える
`nonametag`           プレイヤーのネームタグを見えなくします。（カーソルを合わせると見えます）  
`water`               水に触れると4ダメージ（ハート２つ分のダメージ）を喰らいます。雨でも有効です。  
`invincible`          あらゆる攻撃やダメージを完全に無効化します。（Killコマンドは見事に喰らいます）  
`small`               体が約1メートルほどに小さくなります。  
  
  
### ２，特定のアクションをするとtagがつく  
#### 全て自動でtagがつけられます。  
`sneaking`            スニークすると付くtag  
`sprinting`           走るとつくtag  
`swimming`            泳ぐと付くtag  
`jumping`             ジャンプすると付くtag  
`moving`              動くと付くtag  
`last_hit_by_player`  プレイヤーからダメージを受けると付くtag※1  
`max_health`          体力が最大のときに付くtag  
  
※1 `last_hit_by_player`最後に攻撃してきた相手がプレイヤーだった場合、ずっとtagがついたままになるので注意

重大ミスやリクエストなどtwitterのDMにて　https://twitter.com/masterkamui4649

## ⚠二次配布は配布ワールドに組み込む以外では禁止です。
### 配布ワールドに組み込む場合は http://world-minecraft.com/addon/extra-tag-player-addon かgithubのコメント欄、twitterのDMにてメッセージを一言（使わせていただきます等よろしくおねがいします）
