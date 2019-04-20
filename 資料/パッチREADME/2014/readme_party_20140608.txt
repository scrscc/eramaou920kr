eramaou_party_20140608

※(eramaou　ver.0.302を推奨)

加筆・改変・再アップロードはご自由にどうぞ。

■使い方
　全てのERBファイルをERBフォルダに上書きコピーしてください。

■仕様
　・ダンジョンで勇者達がパーティを組んだ時にメッセージを表示します。
　・メインメニューの能力の表示をしたときに勇者達のパーティの組み合わせが分かります。
　　・PLがパーティリーダー、PMがパーティメンバー、数字が同じなら同じパーティです。

■追加・修正箇所
　■DUNGEON_PARTY.ERB
　123行目と147行目に以下の文を挿入
　IF CHARID == NEW
　		PRINTFORMW %SAVESTR:CHARID%はパーティのリーダーになった！
　ELSE
　		PRINTFORMW %SAVESTR:NEW%は%SAVESTR:CHARID%のパーティに加わった！
　ENDIF
　
　■CHARA_INFO.ERB
　75行目の体力・気力バーを8文字に短縮
　PRINTFORM  HP%BARSTR(BASE:COUNT:0,MAXBASE:COUNT:0,8)% 気%BARSTR(BASE:COUNT:1,MAXBASE:COUNT:1,8)%
　90行目に以下の文を挿入。
	;パーティフラグ
	;パーティメンバー
	IF CFLAG:COUNT:533 > 0 && CFLAG:COUNT:531 == 0 && CFLAG:COUNT:532 == 0 && CFLAG:COUNT:533 != COUNT
		SETCOLOR 255,100,100
		PRINTFORM  PM<{CFLAG:COUNT:533}>
		RESETCOLOR
	;パーティリーダー
	ELSEIF CFLAG:COUNT:533 > 0
		SETCOLOR 255,100,100
		PRINTFORM  PL<{CFLAG:COUNT:533}>
		RESETCOLOR
	ENDIF

　
　
