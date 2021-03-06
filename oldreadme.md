# Extra-tag-player-addon
tagコマンドによりプレイヤーでいろんなことができるようになるアドオンです。  
・・・とかいいつつtagを全く使わない要素も追加する予定です
## ほぼ完全にワールド製作者向けです
## 同梱のリソースパックを入れることでnumberタグを使用可能になります
## ダウンロード [最新版v0.010](https://github.com/GamuKamui/Extra-tag-player-addon/releases/download/v0.010/Extra-tag-player-addon-v0.010.mcaddon)

  
## ※ゲーム内でもtag一覧を見れるようになりました。`/function taghelp`を実行してください
### ⚠まだ開発段階です
## ワールドに導入する方法  
１, このページ一番下の最新版直リンクからデータをダウンロード  
２, ダウンロードしたデータを開く  
３, マイクラが開くので導入したいワールドの設定を開く  
４, ビヘイビアーパックのExtra-tag-player-addonを選んで、使用中の欄に入れる  
５, ワールドを開く  
６, 完成！！  
  
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
        - `small`               体が約1メートルほどに小さくなります。  
  
   - ↓v0.002からの機能  
        - `verysmall` smallよりももっと小さくなります（ハーフブロックの隙間を通れるほど）  
        - `red` `blue` `yellow` `green` 同じタグが付いてる人同士ではフレンドリーファイアしなくなります  
        - `burnlight` ゾンビのように日光にあたると燃えます  
  
   - ↓v0.003からの機能  
        - `big` 体が大きくなります（3mほど）  
        - `verybig` 体がさらに大きくなります（4mほど）  
        - `giveitem` このタグが付いた状態でスニークをしてスニーク解除すると通常では手に入らないアイテムが手に入ります  
       
   - ↓v0.006からの機能  
        - `killanything` どのような状態にあろうともKillします（tagは自動で外れます）（ゲームモードは保持されます）  
        
   - ↓v0.007からの機能  
        - `stevevoice` 被ダメしたときスティーブの声が聞こえるようになります  
        - `notarget` 他MOBから狙われなくなります（すでに狙われていたり攻撃すると狙われます）  
        - `hp(数字)` プレイヤーの最大体力（例えばhp10で最大体力10）最大体力がその数字になります。1～150まであります  
        - `damage(数字)` プレイヤーに一度だけダメージを与えます（例えばdamage10で10ダメージ）1～150まであります。tagは自動で外れます  
        
   - ↓v0.008からの機能  
        - `power(数字)` プレイヤーの攻撃力（例えばpower10で攻撃力10）0～150まであります。  
  
   - ↓v0.009からの機能  
        - `speed(数字)` プレイヤーの移動速度（例えばspeed10で速度10）0～99まであります。(10が規定でそれより下にすると遅くなります)  
        - `noclimd` はしごが登れなくなります  
        
   - ↓v0.010からの機能  
        - `number(数字)` 頭上に数字を表示させます。1～30まであります。
  
  
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
  
   - ↓v0.005からの機能        
        - `gliding` エリトラで滑空すると付きます  
  
   - ↓v0.006からの機能    
        - `pickaxe` どれでもいいのでピッケルを持つと付きます  
        - `axe` どれでもいいのでオノを持つと付きます  
        - `shovel` どれでもいいのでシャベルを持つと付きます  
        - `hoe` どれでもいいのでクワを持つと付きます  
        
   - ↓v0.009からの機能  
        - `killplayer` プレイヤーを倒すと付きます（自動では外れません）  
        
    
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
          
   - ↓v0.006からの機能    
        - 視点の方角をスコアボードに保存できるようになりました  
          保存場所はオブジェクト名`rx`です。  /Function tagrxを常時発動してください  
          `/scoreboard objectives add rx dummy rx`  
        - 視点の高さをスコアボードに保存できるようになりました  
          保存場所はオブジェクト名`ry`です。  /Function tagryを常時発動してください  
          `/scoreboard objectives add ry dummy ry`    
          
   - ↓v0.008からの機能
        - リセット系
          すべてファンクションです。自分以外のプレイヤーで実行させたいときはexecuteコマンドで実行してください  
          `removeall` このアドオンで使われているすべてのタグを外します  
          `removehp` すべてのhpタグを外します  
          `removepower` すべてのpowerタグを外します  
          
   - ↓v0.009からの機能         
        - プレイヤーのキル数をスコアボードに保存することができるようになりました  
          保存場所はオブジェクト名`killcount`です。  
          `/scoreboard objectives add killcount dummy killcount`  
  
   - ↓v0.010からの機能        
        - `numberscorebord`  
        - numberスコアボードの数値を読み取り、numberタグを自動でつけます/function numberscorebord
  
### 修正点  
   - v0.003
        - `invincible`何故かうまく働かなくなったので削除  
          `small`以前まで使っても何も起きていなかったので修正し、使えるように  
          全体のコード一新
   - v0.005  
        - `notburie` 呼吸系がおかしかったので無効化  
   - v0.008  
        - `rx` サーバーに負荷をかける可能性があるためファンクション化しました。/Function tagrxを常時発動してください  
        - `ry` サーバーに負荷をかける可能性があるためファンクション化しました。/Function tagryを常時発動してください  
        - `hp(数字)` 1～150まで使えるように  
        - `damage(数字)` 1～150まで使えるように  
  
   - v0.010  
        - `killanything`    
          ↑function化、/function killanythingで実行です  
        - `removedamage`  
          ↑damageタグは自動で外れなくなりました。/function removedamageで外せます  
  
### 既知のバグ  
   - 修正済み ~~地上でも呼吸ゲージが出ている(その影響か、水中で呼吸ができる)~~  
        - ~~おそらく`notburie`(ブロックの中に埋まってでの窒息ダメージがなくなる)の影響と思われる~~  
   - `attack`攻撃意外での右手を動かすモーション(ボタンを押す、チェストの中を見る時等)でもtagがついている  
   
  
***このアドオンの紹介動画を@kuripasandaさんが作ってくれました！  
本当にありがとう！  
紹介動画→https://youtu.be/i4AUK6J7YA4  
Twitter→https://twitter.com/kuripasanda***  
  
## このアドオンが使用されているワールド↓  
[ネズミバスターズ！！マルチプレイPVPミニゲーム v1.2](http://world-minecraft.com/pe/43768304)  
  
  
  
重大ミスやリクエスト、質問などtwitterのDMにて　https://twitter.com/masterkamui4649  
script apiは不使用なのでWin10版以外でも導入可能です  
  
## ⚠二次配布は配布ワールドに組み込む以外では禁止です。
### 配布ワールドに組み込む場合は http://world-minecraft.com/addon/extra-tag-player-addon かgithubのコメント欄、twitterのDMにてメッセージを一言（使わせていただきます等よろしくおねがいします）

### ⚠配信などで使用する場合、できればでいいのですがこのアドオンの名前(Extra tag player addon)を説明欄等に表記してください。⚠
  
  
  
  
  



  
  
ワールドマインクラフト↓  
http://world-minecraft.com/addon/extra-tag-player-addon  
  
マインアド↓  
https://mineadd.bubbleapps.io/items/1613048866434x204108623241805820  

マインクラフト　コロニー↓  
https://minecraft-mcworld.com/593/
