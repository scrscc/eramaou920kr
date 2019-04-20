eramaou_DRAW_MAINMENU_SHOP_処女献上ver2 20131012

※(eramaou　ver.0.270推奨)

加筆・改変・再アップロードはご自由にどうぞ。

■使い方
　eramaou_0.270パッチまとめ20131005.zipとeramaou_侵略_フィルタ_実験室.zipを適用してから
　全てのERBファイルをERBフォルダに上書きコピーしてください。

■仕様
2013/10/12
・勇者を処刑したときにレベルアップしやすくしました。
・メインメニュー時にTARGET無し、ASSISTANT有り時の表記調整
・体力回復の仕様がおかしかったので修正（午後の調教後の体力回復が大きくなるように）
・処刑後に助手に出来ないキャラが助手になった問題を解決。
・キャラ売却後に助手に出来ないキャラが助手になった問題を解決。
・@EVENTTURNENDの最後に前回の調教対象と前回の助手をTARGETとASSIに戻るように追加。
　この作業はオートセーブ時に@SAVEINFOでやっていたため。これでオートセーブ機能解除時でも問題が無くなるように。

■SYSTEM.ERB
208行目を修正→IF TIME == 1

547行目～549行目に「前回の調教対象と前回の助手を戻す」を追加

■SELL_CHARA.ERB
@KILL_TARGET関数内の助手の情報の取得と助手を戻すを削除

■EXECUTION.ERB
167～177行目にFLAG:1とFLAG:2を空or減算する命令を追加
同様のものを@EXECUTION_MINI関数内に追加

191・232行目を修正→IF FLAG:80 >= CFLAG:0:9

■_DRAW_MAINMENU.ERB
99～101行目に
sif target < 0
PRINTFORM %"",36%
sif target > 0
を追加。

2013/10/11
・_DRAW_MAINMENU.ERBとSHOP.ERBのバグ対策を修正
・メインメニューで助手は無しを選んだ時に以前の助手に戻らないように修正
・処女献上チェックを修正

■EVENT_NEXTDAY.ERB
98～110行目まで処女献上チェックに変更。
OFFERVIRGIN_CHECK関数のチェックに
魔王部屋にいないとダメ
前回の調教対象と同じじゃないとダメ
を追加

■_DRAW_MAINMENU.ERB
8行目を変更→SIF TARGET > CHARANUM - 1

12行目を変更→SIF ASSI > CHARANUM - 1

■SHOP.ERB
7行目を変更→SIF TARGET > CHARANUM - 1

11行目を変更→SIF ASSI > CHARANUM - 1

286行目に追加→FLAG:2 = ASSI


2013/09/29
・貞操帯のカギを捨てれるようにしました。
　↓
・貞操帯のカギを捨てられた子は「迎撃」でダンジョンを探索中に貞操帯のカギを探します。
　↓
・貞操帯のカギを見つけた子はじっくり待って処女を献上しに来ます。

SHOP_TAILOR.ERB
99行目の貞操帯のカギを捨てる条件に再生処女膜不可を追加。
798行目の文章を修正。

DUNGEON.ERB
251行目以降に貞操帯のカギを探す分岐を追加
1/64でカギを発見します。（ちと温いか？）

EVENT_NEXTDAY.ERB
98行目以降のコメントアウトを削除してOFFERVIRGIN_CHECK関数に飛べるように
OFFERVIRGIN_CHECK関数のチェックに
貞操帯の鍵を捨ててないとダメ
貞操帯の鍵を見つけてないとダメ
を追加して貞操帯関係でしか処女献上をしないようにしました。


