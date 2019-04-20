eramaou0.300_LVUPとST_UP修正

前提条件
eramaou_v0.300_パッチまとめ.zip
↓
mayoi_patch.zip
↓
eramaou_能力表示再構成_20140520.zip
↓
eramaou_能力表示再構成の修正1_20140521.zip
↓
eramaou_patch_20140522.zip
↓
eramaou0.300_LVUPとST_UP修正.zip(このパッチ)


修正点
ARCANA_FORT.ERB		CALL ST_UP を CALL ST_UP, A_ARCANA に修正
CHAR_MAKE.ERB		@CHAR_MAKE の CALL ST_UP を CALL ST_UP, Aに修正
			@CHAR_MAKE_INPORT の CALL ST_UP を CALL ST_UP, CHARA に修正
LVUP.ERB		変数AをARG:0に修正、変数XをLOCAL:0に修正
SYSTEM.ERB		CALL LVUP を CALL LVUP, A に修正、$LVUP_REPEAT周辺を修正

