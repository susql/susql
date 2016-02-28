# psql

#### Name
psql --  PostgreSQL interactive terminal

#### Synopsis
psql [option...] [dbname [username]]

#### Meta-Commands

* \d[S+][+] [ pattern ]  
    For each relation (table, view, index, sequence, or foreign table) or composite type matching the pattern,
  show all columns, their types, the tablespace (if not the default) and any special attributes such as NOT NULL or defaults.
  Associated indexes, constraints, rules, and triggers are also shown.
  For foreign tables, the associated foreign server is shown as well. 
  ("Matching the pattern" is defined in Patterns below.)  
  **[+] more than one** (sample: \d++) will show you addition information such as STORED AS and COMPRESS information.
