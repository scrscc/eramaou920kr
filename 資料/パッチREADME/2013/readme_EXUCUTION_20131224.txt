eramaou_EXUCUTION_20131224パッチ

※(eramaou　ver.0.280推奨)

加筆・改変・再アップロードはご自由にどうぞ。

■使い方
　全てのERBファイルをERBフォルダに上書きコピーしてください。

■仕様
　処刑時に最後の一言を言うようになります。
　一言ずつしか書いてないので物足りなかったらバンバン追加してね！
　battle_word_patch.zipを適用しています。

■修正箇所
　■EXUCUTION.ERB
	97行目に以下を追加。
	TFLAG:16 = RESULT
	CALL EXUCUTION_KOUJO

	101行目から163行目のIF文の条件をRESULTからTFLAG:16に変更
	このTFLAG:16は@EXUCUTION_KOUJO_KXX口上で使用します。

　■EVENT_K.ERB
	末尾に@EXUCUTION_KOUJO関数を追加。

　■EVENT_K_DUMMY.ERB
	末尾に処刑関連のダミー関数を追加。

　■EVENT_K0.ERB
　■EVENT_K1.ERB
　■EVENT_K2.ERB
　■EVENT_K3.ERB
　■EVENT_K4.ERB
　■EVENT_K5.ERB
　■EVENT_K6.ERB
	末尾に@EXUCUTION_KOUJO_KXX関数を追加。
	会話時のビデオ自己紹介成功時に
	TFLAG:32 |= 2
	を追加。


