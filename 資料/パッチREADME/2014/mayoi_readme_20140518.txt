
何故か後続の勇者が迷っていたD:2の迷いフラグを機能させるパッチです

おまけつき

フラグまとめ
　CFLAG:509 = 迷いフラグ

DNGEON.ERB
DUNGEON_TRAP.ERB
DUNGEON_ROOM.ERB
D:2 を CFLAG:A:509 に入れ替え

MONSTER_SKILL.ERB
D:1 は迷いフラグだったはずなので CFLAG:(ARG:0):509 に入れ替え

DNGEON.ERB
永遠に迷うのを防ぐため判定を変更

*おまけ*

DUNGEON_BATLLE.ERB
DUNGEON_BATLLE2.ERB
実装を忘れていた先制不可フラグを実装

DUNGEON_ROOM.ERB
RETURN 0が2個あった所を修正
毒蟲の指定ミスを修正
実装を忘れていた人間牧場の拡張を追加


*指摘があったので追加しました*
すみません

MAGIC.ERB
LABO_DUNGEON_MAP.ERB
D:2 を CFLAG:A:509 に入れ替え




