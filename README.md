# Kozakura DB - A Kanji by Radicals SQLite Database

KozakuraDB is a SQLite database file compiled from the [radkfile](http://nihongo.monash.edu//kradinf.html) and [kanjidic2](http://www.edrdg.org/wiki/index.php/KANJIDIC_Project) files.

## Structure
The database contains three tables:  
Kanji (id INTEGER PRIMARY KEY, lit TEXT, strokes INTEGER)  
Rad (id INTEGER PRIMARY KEY, lit TEXT, strokes INTEGER)
* id is the int32 scalar value of the UTF-8 encoding of the character.
* lit is the utf8 encoded string of the character.
* strokes is the number of strokes of the character in int32.  

KanjiByRad (rad INTEGER, kanji INTEGER, PRIMARY KEY(rad, kanji)
* rad is the id of the radical
* kanji is the id of the kanji


## License

This work is provided under a **Creative Commons Attribution-ShareAlike Licence (V3.0)**. The Licence Deed can be viewed [here](https://creativecommons.org/licenses/by-sa/3.0/), and the full Licence Code is [here](https://creativecommons.org/licenses/by-sa/3.0/legalcode).

This publication uses material from the [radkfile](http://nihongo.monash.edu//kradinf.html) and [kanjidic2](http://www.edrdg.org/wiki/index.php/KANJIDIC_Project) dictionary files. These files are property of the [Electronic Dictionary Research and Development Group](http://www.edrdg.org/) and are used in accordance with the licence provisions of the Electronic Dictionaries Research Group. See http://www.edrdg.org/edrdg/licence.html
