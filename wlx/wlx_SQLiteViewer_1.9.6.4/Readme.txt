SQLiteViewer 1.9.6.4
Simple plugin for TC for view SQLite database files. Supports *.db, *.db3, *.sqlite, *.sqlite3 and *.fossil extensions.

Supports up to 2TB files, no sqlite3.dll needed.
Supports data types described in this document:
http://www.sqlite.org/datatype3.html

About auto creating any additional files when some database viewing (and open these databases from read-only sources):
http://www.sqlite.org/tempfiles.html#walfile
http://www.sqlite.org/wal.html


License agrement
This software provided "AS-IS" without warranty of any kind for non-commercial use only.


Changes history

Ver 1.0:
 * public release.

Ver 1.5:
 * more SQLite database files support;
 + new DetectString extension: sqlite (reinstall plugin or add it manually);
 * bug fixes.

Ver 1.6:
 + columns autosize when open table (check limit to 1000 records for speed purposes);
 + column autosize by double click on columns divider;
 + sort by column header clicking;
 + table info;
 * other fixes.

Ver 1.6.1:
 * some UI changes;
 * other fixes.

Ver 1.6.2:
 + current record can be copied to Clipboard as CRLF separated strings.

Ver 1.7:
 + some BLOB fields displayed as string now;
 + tables list panel can be displayed (switch on in ini);
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   ShowTablesPanel=0 - on/off tables panel (default 0)
   BlobAsText=1 - on/off BLOB fields as text (default 1)
   BlobAsTextLimit=150 - characters limit for BLOB as text (20..255, default 150);
 * other fixes.

Ver 1.7.5:
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   FixDrawErrors=1 - in some cases remove flickering
   FixScrollError=0 - do not go to first column when scroll using thumb
   FixDrawScrollError=0 - when FixScrollError=1 in some cases remove flickering (on old PC is slow)
   GridOddRowOtherColor=1 - use other color for odd row
   GridOddRowColor=$00F4F4F4 - color of odd row;

Ver 1.7.6:
 * may be used standard lsplugin.ini for read settings.

Ver 1.8:
 * updated database engine;
 * database opens as read only now (PRAGMA query_only);
 * fixed show tables with spaces in name;
 + double click on grid row opens Record View window;
 * BlobAsTextLimit may be increased up to 2000 characters (20..2000, default 150);
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   ShowTablesCombobox=1 - on/off tables combobox (default 1)
   StringLengthLimit=255 - characters limit for string (20..2000, default 255)
  ! Warning. After set up limit for Blob and string bases with huge records may not be opened by out of memory.
   SkipSystemTables=0 - don't add to list tables whose names starts from "sqlite_" (default 0);
 * other fixes.

Ver 1.8.1:
 * other fixes.

Ver 1.8.2:
 * updated database engine;
 * plugin recompiled in Delphi XE4 for stability issues on x64 versions of Windows;
 + show table info in SQL format;
 * wrong sorting when right click on grid header and next any inside;
 * other fixes.

Ver 1.8.3:
 * updated database engine;
 + support tables created with "WITHOUT ROWID" phrase (https://www.sqlite.org/withoutrowid.html).

Ver 1.8.4:
 * updated database engine;
 + new DetectString extensions: sqlite3 and fossil (reinstall plugin or add it manually).

Ver 1.8.5:
 * updated database engine;
 + simple filter using LIKE for all fields, standard TC Lister search dialog (without options) (F7).

Ver 1.8.6:
 * updated database engine;
 * now filter for unicode words supports case insensitive and can use options from standard TC Lister search dialog (F7);
 + simple filter dialog.

Ver 1.8.7:
 * updated database engine;
 + filter options Not Contain and Just Not Empty.

Ver 1.9.0:
 * updated database engine;
 + add support for VIEW's.
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   AddVIEWs=1 - add VIEW's to the table list (default 1)
 + Setup dialog (menu item Setup...);
 * other fixes.

Ver 1.9.1:
 * updated database engine;
 + show current record number (need enable in Setup dialog).
 * other fixes.

Ver 1.9.2:
 * updated database engine;
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   DatabaseReadOnly=1 - open database in read only mode (default 1);
 * other fixes.

Ver 1.9.3:
 * behavior of TAB button fixed in TC x64;
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   SpecialCheckQuery=0 - if database opened in read/write mode (DatabaseReadOnly=0) and query not start from 'select' then reopen table or database after query (default 0).

Ver 1.9.5:
 * updated database engine;
 + SQLiteViewer.ini for manual setup:
   [SQLiteViewer]
   FixDateTimeField=1 - try properly show DATETIME fields (default 1).

Ver 1.9.6:
 * updated database engine;
 + allow delete current record (if database opened in read/write mode (DatabaseReadOnly=0)).

Ver 1.9.6.1:
 * updated database engine;
 + sort tables names (view's names sort separately).

Ver 1.9.6.2:
 * strings sorting fixed.

Ver 1.9.6.3:
 * updated database engine;
 * other fixes.

Ver 1.9.6.4:
 * other fixes.


---
Suggestions, Wishes and bug reports are welcome!
ProgMan13, (ProgMan13@mail.ru)