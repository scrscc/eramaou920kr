
eramaou0.301_MONSTER_DATA修正パッチを当ててからこのパッチを適用してください

DUNGEON_BATTLE2.ERB	配下モンスターデータの取得・モンスターの攻撃呼び出し前に条件を追加
			SPEED_PLUS2の処理をSPEED_PLUSに合わせる
			@SLAVE_MONSTER_ATTACK_TO_ENEMYと@SLAVE_MONSTER_ATTACK_TO_SLAVEから変数E以外の一文字変数を削除
			@DEATH_CHECK2から一文字変数を削除

追加修正
DUNGEON_BATTLE2.ERB	75-76行目の変数Tを変数Bに修正

