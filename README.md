#   K o z a k u r a   D B   - A Kanji by Radicals SQLite Database

KozakuraDB is a SQLite database file compiled from kanjidic2 and radkfile.

The database contains two tables:
Kanji (id INTEGER PRIMARY KEY, lit TEXT, strokes INTEGER)
Rad (id INTEGER PRIMARY KEY, lit TEXT, strokes INTEGER, kanji BLOB)

* id is the int32 scalar value of the UTF-8 encoding of the character.
* lit is the utf8 encoded string of the character.
* strokes is the number of strokes of the character in int32.
* kanji is the list of kanji associated with the radical.
	The format of the blob is a sequence of int32 values, used as id in the Kanji table.
	Each value is the int32 scalar value of the UTF-8 encoding of a character.
	The bytes of the int32 are stored in little-endian.
	For example the Kanji 札 with id 0x00_00_67_2D will be stored as 0x2D_67_00_00


This publication has included material from the JMdict (EDICT, etc.) dictionary files in accordance with the licence provisions of the Electronic Dictionaries Research Group. See http://www.edrdg.org/
 
