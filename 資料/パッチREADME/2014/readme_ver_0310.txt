
-----------------------------------
  今回の更新
-----------------------------------
Talent.csv
ARCANA_BATTLE.ERB
CHAR_MAKE.ERB
COMF87.ERB
DUNGEON_BATLLE.ERB
DUNGEON_BATLLE2.ERB
EVENT_K4.ERB
EVENT_PREGNANCY.ERB
EVENT_TRAIN_MESSAGE_A.ERB
LOOK.ERB
MAGIC.ERB
MARRIAGE_DAY.ERB
MONSTER_SKILL.ERB
SHOP_LABO.ERB
SYSTEM.ERB

-----------------------------------
  モンスター戦改良
-----------------------------------

◆攻撃処理一本化
DUNGEON_BATLLE2.ERB
ARCANA_BATTLE.ERB

キャラからキャラへの攻撃を
DUEL_ATTACKに一本化
いくつかの旧処理を完全削除
@ARCANA_BATTLE
変数を設定

◆忍術のスキルを回避能力に変更
DUNGEON_BATLLE.ERB
DUNGEON_BATLLE2.ERB
回避率15%上昇

◆ボスへの魔法ダメージを1/10に
MAGIC.ERB

◆モンスタースキルの発動確率設定と強化
MONSTER_SKILL.ERB
発動確率を2/3に
威力を2倍に強化

◆コメントを少々追加
DUNGEON_BATLLE.ERB
DUNGEON_BATLLE2.ERB
ARCANA_BATTLE.ERB

-----------------------
	地の文加筆
-----------------------
EVENT_TRAIN_MESSAGE_A.ERBを主に加筆

◆愛撫の分岐を追加

-----------------------
	結婚生活強化
-----------------------
MARRIAGE_DAY.ERBを主に加筆

◆魔王様の結婚生活実装
@MARRIAGE_DAY_YOU

◆犬のお嫁さん強化
@MARRIAGE_DAY_DOG

◆亜人のお嫁さん強化
@ORC_MARRIAGE_DAY

-----------------------------------
  ふたなり強化
-----------------------------------

◆ペニスの状態を追加
Talent.csv
318 ペニスの状態

LOOK.ERB
@LOOK_INFO
ペニスの状態表記
@LOOK_SET
ペニスの初期設定

◆地の文にペニスの状態反映
EVENT_TRAIN_MESSAGE_A.ERB

◆ペニスがあると自慰経験が増える
CHAR_MAKE.ERB
自慰経験の初期設定
ついでにふたなり生成時に童貞を追加

◆ふたなり改造でペニスの状態を選べるように
SHOP_LABO.ERB
馬ペニスというものがあるらしい

-----------------------
	小ネタ
-----------------------

◆人狼が満月のときに妊娠しやすいように
EVENT_PREGNANCY.ERB
234行目辺り

◆戦闘スキップ中の停止で全戦闘終了後にもう一度停止
SYSTEM.ERB
493行目辺り


-----------------------
	バグフィックス
-----------------------

◆冷徹口上の誤字修正
EVENT_K4.ERB
1089行目

◆ピアスのバグについて
COMF87.ERB
81行目

-----------------------
	今後の予定
-----------------------
予定は未定

◆口上追加
知的口上（ハカセタイプ・進捗60%）
庇護者口上（ママさんタイプ・進捗0%）

◆奴隷売却先を選択式に
鬼畜ルートとか幸せルートとか選べる感じ…
でも時間がかかりそうなので先にパッチ作っちゃったぜ！も歓迎します

◆アクティブスキル追加
勇者や奴隷が通常攻撃の代わりに発動させるスキルの追加

いまの戦闘はただ順番に殴り合う退屈な物なので
なにか発動させるスキルでも追加したいです

気力と体力が十分にある状態で、確率発動
パーティ全体バフや強い攻撃など…仕様が固まったら



