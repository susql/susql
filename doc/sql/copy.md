# COPY

#### Name
COPY -- copy data between a file and a table

#### Synopsis
```
COPY table_name [ ( column_name [, ...] ) ]
    FROM { 'filename' | PROGRAM 'command' | DIRECTORY 'directory_name' [ RECURSIVE { 'NUMBER' } ] | STDIN }
    [ [ WITH ] ( option [, ...] ) ]

COPY { table_name [ ( column_name [, ...] ) ] | ( query ) }
    TO { 'filename' | PROGRAM 'command' | STDOUT }
    [ [ WITH ] ( option [, ...] ) ]

where option can be one of:

    FORMAT format_name
    OIDS [ boolean ]
    FREEZE [ boolean ]
    DELIMITER 'delimiter_character'
    NULL 'null_string'
    HEADER [ boolean ]
    QUOTE 'quote_character'
    ESCAPE 'escape_character'
    FORCE_QUOTE { ( column_name [, ...] ) | * }
    FORCE_NOT_NULL ( column_name [, ...] )
    FORCE_NULL ( column_name [, ...] )
    ENCODING 'encoding_name'
    UNSTRICT [ boolean ]
    UNSTRICT_NUM { number }
```

#### Parameters

* DIRECTORY
  Indicates the input is a directory and will copy all file in this directory.
  * RECURSIVE {NUMBER}
  Specifies if the recusive directory copy will be applied.

* UNSTRICT
  Specifies that whether continue copy process when some line is broken.  
  
* UNSTRICT_NUM
  Specifies how many broken lines reach to stop the copy process. Only effects when UNSTRICT is set.


