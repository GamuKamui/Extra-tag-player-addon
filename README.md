# Extra-tag-player-addon  
# エクストラ-タグ-プレイヤー-アドオン  

tagコマンドによりプレイヤーでいろんなことができるようになるアドオンです。  
・・・とかいいつつtagを全く使わない要素も追加する予定です
#### ほぼ完全にワールド製作者向けです
#### 同梱のリソースパックを入れることでnumber、imageタグを使用可能になります
## ダウンロード [最新版v0.012](https://github.com/GamuKamui/Extra-tag-player-addon/releases/download/v0.012/Extra-tag-player-addon-v0.012.mcaddon).[改造用リソースパック.zip](https://github.com/GamuKamui/Extra-tag-player-addon/releases/download/v0.011/Extra-tag-player-addonR-v0.011.zip)
   
## 軽量化バージョンも作成しています  
[軽量バージョンv0.012-lite-1](https://github.com/GamuKamui/Extra-tag-player-addon/releases/tag/v0.012-lite-1)  
[軽量バージョンv0.012-lite-1v2](https://github.com/GamuKamui/Extra-tag-player-addon/releases/tag/v0.012-lite-1v2)  
  
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
   - `nonametag`           プレイヤーのネームタグを見えなくします。（カーソルを合わせると見えます）  
   - `water`               水に触れるとダメージを喰らいます。雨でも有効です。  
   - `small`               体が約1メートルほどに小さくなります。  
   - `verysmall` smallよりももっと小さくなります（ハーフブロックの隙間を通れるほど）  
   - `red` `blue` `yellow` `green` 同じタグが付いてる人同士ではフレンドリーファイアしなくなります  
   - `burnlight` ゾンビのように日光にあたると燃えます  
   - `big` 体が大きくなります（3mほど）  
   - `verybig` 体がさらに大きくなります（4mほど）  
   - `giveitem` このタグが付いた状態でスニークをしてスニーク解除すると通常では手に入らないアイテムが手に入ります  
   - `stevevoice` 被ダメしたときスティーブの声が聞こえるようになります  
   - `notarget` 他MOBから狙われなくなります（すでに狙われていたり攻撃すると狙われます）  
   - `hp(数字)` プレイヤーの最大体力（例えばhp10で最大体力10）最大体力がその数字になります。1～150まであります  
   - `damage(数字)` プレイヤーに一度だけダメージを与えます（例えばdamage10で10ダメージ）1～150まであります。tagは自動で外れます  
   - `power(数字)` プレイヤーの攻撃力（例えばpower10で攻撃力10）0～150まであります。  
   - `speed(数字)` プレイヤーの移動速度（例えばspeed10で速度10）0～99まであります。(10が規定でそれより下にすると遅くなります)  
   - `noclimd` はしごが登れなくなります  
   - `number(数字)` 頭上に数字を表示させます。1～30まであります。  
   - `image(数字)` 頭上に画像を表示させます。1～70まであります。リソースパックを改造して好きな画像を表示できます。  
   - `notextraplayer` 一部影響を与えるタグの判定を通り抜けます（処理が重くなる人向け）通り抜けるタグ↓
     `nonametag water small verysmall burnlight big verybig notarget hp(数字) damage(数字) power(数字) speed(数字) noclimd number(数字) image(数字)`
   - `extraplayer` ↑とは逆に今すぐにタグの判定をします。自動で外れます。内部処理で2秒毎についたり外れたりします。
  
  
### ２，特定のアクションをするとtagがつく  
#### 全て自動でtagがつけられます。  
   - `sneaking`            スニークすると付くtag  
   - `sprinting`           走るとつくtag  
   - `swimming`            泳ぐと付くtag  
   - `jumping`             ジャンプすると付くtag  
   - `moving`              動くと付くtag  
   - `last_hit_by_player`  プレイヤーからダメージを受けると付くtag（自動では外れません）  
   - `max_health`          体力が最大のときに付くtag  
   - `deathplayer` プレイヤーによって殺された場合に付きます。（自動では外れません）  
     同時にスコアボードにデス数を記録します  
     `/scoreboard objectives add deathplayer dummy deathplayer`  
   - `death` 死亡したときに付きます（自動では外れません）  
   - `damage` 被ダメージしたときに付きます（自動では外れません）  
   - `helmet`何でもいいのでヘルメットをかぶったときに付きます  
   - `chestplate`何でもいいのでチェストプレートを付けた時に付きます  
   - `leggings`何でもいいのでレギンスを履いた時に付きます  
   - `boots`何でもいいのでブーツを履いた時に付きます        
   - `sword` どれでもいいので剣を持つと付きます  
   - `attack` 攻撃モーション時に付きます（自動では外れません）  
   - `using` 何らかのアイテムを使用したときに付きます（何かを食べる、弓矢をかまえる等）  
   - `onfire` 体が燃えているときに付きます      
   - `gliding` エリトラで滑空すると付きます    
   - `pickaxe` どれでもいいのでピッケルを持つと付きます  
   - `axe` どれでもいいのでオノを持つと付きます  
   - `shovel` どれでもいいのでシャベルを持つと付きます  
   - `hoe` どれでもいいのでクワを持つと付きます  
   - `killplayer` プレイヤーを倒すと付きます（自動では外れません）  
        
    
### ３，tagとは無関係  
   - スコアボードに体力を記録できるようになりました。  
     保存場所はオブジェクト名`hp`です。  
     `/scoreboard objectives add hp dummy hp`  
        
   - なんのアイテムを持っているかをスコアボードに保存することができるようになりました  
     保存場所はオブジェクト名`haveitem`です。  
     `/scoreboard objectives add haveitem dummy haveitem`  
     ちなみにビヘイビアのドキュメントにあるアイテムIDで保存してますが  
     普通ではググっても出てこないので[ItemID](https://github.com/GamuKamui/Extra-tag-player-addon/blob/main/itemID/)で見てください。  
     （とかいいつつ、このアイテム持ったらこのスコアなんだな、とか自分で見たほうが早いと思います。）  

   - 視点の方角をスコアボードに保存できるようになりました  
     保存場所はオブジェクト名`rx`です。  /Function tagrxを常時発動してください  
     `/scoreboard objectives add rx dummy rx`  
   - 視点の高さをスコアボードに保存できるようになりました  
     保存場所はオブジェクト名`ry`です。  /Function tagryを常時発動してください  
     `/scoreboard objectives add ry dummy ry`    

   - リセット系
     すべてファンクションです。自分以外のプレイヤーで実行させたいときはexecuteコマンドで実行してください  
     `removeall` このアドオンで使われているすべてのタグを外します  
     `removehp` すべてのhpタグを外します  
     `removepower` すべてのpowerタグを外します  
            
   - プレイヤーのキル数をスコアボードに保存することができるようになりました  
     保存場所はオブジェクト名`killcount`です。  
     `/scoreboard objectives add killcount dummy killcount`  

   - `numberscorebord`  
     numberスコアボードの数値を読み取り、numberタグを自動でつけます/function numberscorebord
  
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
   - v0.010a  
        - コード一新、tagがついている判定を1秒に1回に変更
   - v0.010c  
        - damage(数字)タグ最適化、自動で外れるように
        - tagがついている判定が前回修正で1秒に2回判定していたらしいので2秒に1回に修正
  

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
