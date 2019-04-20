eramaou0.300_DUMMY削除

前提条件
eramaou_ご褒美口上パッチ_20140515
※パッチ適用後、EVENT_K_DUMMY.ERBを削除してください


修正点
EVENT_K.ERB	変数CをLOCALに置き換え、CALLをTRYCALLFORMに置き換え
EVENT_K0.ERB	BENKI_KOUJO_K0がなかったのでテンプレートから移植
EVENT_K1.ERB	BENKI_KOUJO_K1がなかったのでテンプレートから移植
EVENT_K2.ERB	BENKI_KOUJO_K2がなかったのでテンプレートから移植
EVENT_K3.ERB	RAND:1 == 0 があったので周辺部分をRAND:4～RAND:2に修正
		BENKI_KOUJO_K3がなかったのでテンプレートから移植

未修正点
・口上の一部で変数AとTARGETが混在している部分が割とある(動作上は問題なし？)
　例)EVENT_K5.ERB	IF (BASE:A:0 * 100 / MAXBASE:A:0 < 50) || (BASE:A:1 * 100 / MAXBASE:A:1 < 50)
				PRINTFORMW %SAVESTR:TARGET%は壁を背にしてへたり込んだ。
・各口上の ;@KOJO_MESSAGE_PALAMCNG関係（X1をキャラ番号に置換
　数行下のSIF ～ RETURN 0 条件式が口上ファイルごとに結構異なっている


log.txt
パッチ作成前はemueraの解析機能で「定義されていますが一度も呼び出されません」エラーが表示されてたのに
パッチ適用後に表示されなくなった(該当箇所は未修正のまま)
emuera側の不具合？

