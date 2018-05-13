# Android_S11_A1

Q1: What is the use of SQLite open helper class in SQLLite?

Answer:

A helper class to manage database creation and version management.
You create a subclass implementing onCreate(SQLiteDatabase), onUpgrade(SQLiteDatabase, int, int) and optionally onOpen(SQLiteDatabase), and this class takes care of opening the database if it exists, creating it if it does not, and upgrading it as necessary. Transactions are used to make sure the database is always in a sensible state.
This class makes it easy for ContentProvider implementations to defer opening and upgrading the database until first use, to avoid blocking application startup with long-running database upgrades.

Q2: What is the use of OnUpgrade function in SQLiteOpenHelper class?

Answer:

onUpgrade() is only called when the database file exists but the stored version number is lower than requested in constructor. The onUpgrade() should update the table schema to the requested version.


Q3: How to show SQlite database table information in Android application what is the best way to do it?


Answer:

Showing data base information will be better suited with table layout. Since table layout is not an adapter view, you can't use cursor adapter with it. So use table layout with cursor to show data base table information.
