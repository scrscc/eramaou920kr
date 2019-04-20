eramaou_patch_20150228

※(eramaou　ver.0.340推奨)

加筆・改変・再アップロードはご自由にどうぞ。

■使い方
　全てのERBファイルをERBフォルダに上書きコピーしてください。

■仕様
・結婚していたら一度離婚しないと再婚出来ないようにしました。
・バグ修正。アイテムとの結婚が出来ないようにしました。
・バグ修正。RAND:0にならないように@NAKADASHI_CHECK関数を修正しました。
・バグ修正。あなたと奴隷が結婚した時に従順が３以上なければ止まるバグを修正しました。

■追加・修正箇所
　■CHARA_MARRIAGE.ERB
　　モンスター以外のアイテムを排除するために
　　83行目に以下の分岐を追加。
　　ELSEIF RESULT <= 99
		PRINTL それはアイテムです
		GOTO INPUT_LOOP
	89行目に以下の分岐を追加。
	ELSEIF CFLAG:ARG:601 > 0
		PRINTFORMW %SAVESTR:ARG%はすでに結婚している
	RETURN 0

　■EVENT_PREGNANCY.ERB
　　可読性を上げるために@NAKADASHI_CHECK関数に以下の#DIMを設定してLOCAL:0とLOCAL:1を置換。
	#DIM NAKADASHI_PARTNER
	#DIM HAIRANZAI
　　236行目以降を以下に修正
　　;人狼の場合、満月時に妊娠しやすく
　　IF TALENT:(ARG:0):314 == 2 && DAY:2 >= 14 && DAY:2 <= 16 && CFLAG:(ARG:0):109 == 1
		HAIRANZAI = 1
　　ELSEIF TALENT:(ARG:0):314 == 2 && DAY:2 >= 14 && DAY:2 <= 16
		HAIRANZAI = 2
　　ENDIF

　■MARRIAGE_DAY.ERB
　　ケアレスミスがあったので修正。
　　200行目を以下に修正
　　PRINTFORML %SAVESTR:A%はあなたと暮らしている。
　　221行目を以下に修正
　　ELSEIF MARK:A:3 >= 1

　
