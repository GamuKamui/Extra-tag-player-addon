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
[他の例](https://github.com/GamuKamui/Extra-tag-player-addon/blob/main/rei.md)  
  
  
## tag説明 
### １，特定のtagをつけるとプレイヤーに影響を与える
   - ↓v0.001からの機能
        - `nonametag`           プレイヤーのネームタグを見えなくします。（カーソルを合わせると見えます）  
        - `water`               水に触れると4ダメージ（ハート２つ分のダメージ）を喰らいます。雨でも有効です。  
        - `invincible`          あらゆる攻撃やダメージを完全に無効化します。（Killコマンドは見事に喰らいます）  
        - `small`               体が約1メートルほどに小さくなります。  
  
   - ↓v0.002からの機能  
        - `verysmall` smallよりももっと小さくなります（ハーフブロックの隙間を通れるほど）  
        - `red` `blue` `yellow` `green` 同じタグが付いてる人同士ではフレンドリーファイアしなくなります  
        - `burnlight` ゾンビのように日光にあたると燃えます  
        - `notburie` ブロックの中に埋まってでの窒息ダメージがなくなります  
  
   - ↓v0.003からの機能  
        - `big` 体が大きくなります（3mほど）  
        - `verybig` 体がさらに大きくなります（4mほど）  
        - `giveitem` このタグが付いた状態でスニークをしてスニーク解除すると通常では手に入らないアイテムが手に入ります  
  
  
### ２，特定のアクションをするとtagがつく  
#### 全て自動でtagがつけられます。  
   - ↓v0.001からの機能
        - `sneaking`            スニークすると付くtag  
        - `sprinting`           走るとつくtag  
        - `swimming`            泳ぐと付くtag  
        - `jumping`             ジャンプすると付くtag  
        - `moving`              動くと付くtag  
        - `last_hit_by_player`  プレイヤーからダメージを受けると付くtag（自動では外れません）  
        - `max_health`          体力が最大のときに付くtag  
  
   - ↓v0.002からの機能  
        - `deathplayer` プレイヤーによって殺された場合に付きます。（自動では外れません）  
          同時にスコアボードにデス数を記録します  
          `/scoreboard objectives add deathplayer dummy deathplayer`  
  
   - ↓v0.003からの機能  
        - `death` 死亡したときに付きます（自動では外れません）  
        - `damage` 被ダメージしたときに付きます（自動では外れません）  
        - `helmet`何でもいいのでヘルメットをかぶったときに付きます  
        - `chestplate`何でもいいのでチェストプレートを付けた時に付きます  
        - `leggings`何でもいいのでレギンスを履いた時に付きます  
        - `boots`何でもいいのでブーツを履いた時に付きます  
        
   - ↓v0.004からの機能        
        - `sword` どれでもいいので剣を持つと付きます  
        - `attack` 攻撃モーション時に付きます（自動では外れません）  
        - `using` 何らかのアイテムを使用したときに付きます（何かを食べる、弓矢をかまえる等）  
        - `onfire` 体が燃えているときに付きます  


### ３，tagとは無関係  
   - ↓v0.002からの機能   
        - スコアボードに体力を記録できるようになりました。  
        - 保存場所はオブジェクト名`hp`です。  
        - `/scoreboard objectives add hp dummy hp`  
        
   - ↓v0.004からの機能        
        - なんのアイテムを持っているかをスコアボードに保存することができるようになりました  
          保存場所はオブジェクト名`haveitem`です。  
          `/scoreboard objectives add haveitem dummy haveitem`  
          ちなみにビヘイビアのドキュメントにあるアイテムIDで保存してますが  
          普通ではググっても出てこないので[ItemID](https://github.com/GamuKamui/Extra-tag-player-addon/blob/main/itemID/)で見てください。  
          （とかいいつつ、このアイテム持ったらこのスコアなんだな、とか自分で見たほうが早いと思います。）  
  
  
### 修正点  
   - v0.003
        - `invincible`何故かうまく働かなくなったので削除  
          `small`以前まで使っても何も起きていなかったので修正し、使えるように  
          全体のコード一新
  
  
  
  
  
  
  
  

重大ミスやリクエストなどtwitterのDMにて　https://twitter.com/masterkamui4649

## ⚠二次配布は配布ワールドに組み込む以外では禁止です。
### 配布ワールドに組み込む場合は http://world-minecraft.com/addon/extra-tag-player-addon かgithubのコメント欄、twitterのDMにてメッセージを一言（使わせていただきます等よろしくおねがいします）
