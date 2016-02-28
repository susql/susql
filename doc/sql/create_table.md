# CREATE TABLE

#### Name
CREATE TABLE -- define a new table

#### Synopsis

```
CREATE [ [ GLOBAL | LOCAL ] { TEMPORARY | TEMP } | UNLOGGED ] TABLE [ IF NOT EXISTS ] table_name ( [
  { column_name data_type [ COLLATE collation ] [ column_constraint [ ... ] ]
    | table_constraint
    | LIKE source_table [ like_option ... ] }
    [, ... ]
] )
[ INHERITS ( parent_table [, ... ] ) ]
[ WITH ( storage_parameter [= value] [, ... ] ) | WITH OIDS | WITHOUT OIDS ]
[ ON COMMIT { PRESERVE ROWS | DELETE ROWS | DROP } ]
[ TABLESPACE tablespace_name ]
[ STORED AS { HEAP | ORC } ]
[ SORT BY { column_name [,...]}]
```

#### Parameters
* STORED AS  
  * HEAP: row storage format(postgres heap)(**default**).
  * ORC:  column storage format.

* SORT BY  
  When table is STORED AS **ORC**, sort the column for reading optimize.
