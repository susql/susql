# CREATE TABLE

#### Name
CREATE TABLE -- define a new table

#### Synopsis

```
CREATE [ [ GLOBAL | LOCAL ] { TEMPORARY | TEMP } | UNLOGGED ] TABLE [ IF NOT EXISTS ] table_name ( [
  { column_name data_type [ COLLATE collation ] [ COMPRESS compression ] [ column_constraint [ ... ] ]
    | table_constraint
    | LIKE source_table [ like_option ... ] 
    | COMPRESS default_compression }
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

* COMPRESS  
  To set column compression type for a table. **COMPRESS default_compression** is for default compression type if individual column compression is not specific.  
  There is a buildin compression type **PGLZ**, and an extension compression type **ZLIB**(create extension dc_zlib fistly to use ZLIB compression).  

