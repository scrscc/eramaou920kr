eramaou_patch_20140522

※(eramaou　ver.0.300+各種パッチファイルの適用を推奨)

加筆・改変・再アップロードはご自由にどうぞ。

■前提条件
eramaou_v0.300_パッチまとめ.zip
↓
mayoi_patch.zip
↓
eramaou_能力表示再構成_20140520.zip
↓
eramaou_能力表示再構成の修正1_20140521.zip
以上を適用してから使って下さい。

■使い方
　ARCANA_FORT.ERB
　DUNGEON_ROOM.ERB
　MAGIC.ERB
　SHOP.ERB
　以上のERBファイルをERBフォルダに上書きコピーしてください。

■仕様
・ARCANA_FORT.ERBの1文字変数を出来るだけ減らした。
・アルカナナイトの名前を元に戻した時に「メアリー」以外になるようにしました（命名はランダム）。
・アルカナナイトとの戦いに挑んだときに元勇者が全裸の時のメッセージ追加。
・商店街と人間牧場の特定階層が毎晩チェックされない不具合を修正。
・魔法使用時の誤字を修正。
・メインメニューの奴隷と助手を選んだときの名前とライフバーの二重表示を修正。

■追加・修正箇所
　■ARCANA_FORT.ERB
　　1文字変数をTMP_ARCANA　TMP2_ARCANA　Y_ARCANA　A_ARCANAに変更。
　　しかし、レベルアップ処理とARCANA_BATTLE.ERBでどうしても1文字変数A,Bを使用することに。
　　CFLAG:6にランダムネームを記憶するように。

　■DUNGEON_ROOM.ERB
　　@DUNGEON_ROOM_DAYのROOMID += 1を削除
　　
　■MAGIC.ERB
　　誤字を修正。

　■SHOP.ERB
　　メインメニューの奴隷と助手を選ぶと名前とライフバーが二重に表示されるので144行目以降を以下に修正。
　　ELSEIF RESULT == 498
　　	CALL CHARA_INFO_INDIVIDUAL, TARGET
　　ELSEIF RESULT == 499
　　	CALL CHARA_INFO_INDIVIDUAL, ASSI

	@SELECT_TARGETと@SELECT_ASSIのB = RESULTを削除

