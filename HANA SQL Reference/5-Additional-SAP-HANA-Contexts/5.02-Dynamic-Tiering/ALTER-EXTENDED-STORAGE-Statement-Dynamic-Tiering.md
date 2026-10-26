# 5.2.3 ALTER EXTENDED STORAGE Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1219–1222

Lets you manage the extended storage space.

## Syntax

```sql
ALTER EXTENDED STORAGE [<enable_delta_clause>] [<add_dbfile_clause>]
      [<empty_dbfile_clause>] [<drop_dbfile_clause>]
[<increase_dbfile_size_clause>]
```

## Syntax Elements

#### enable_delta_clause

Create a delta dbspace or disable delta dbspace creation in extended storage. Delta dbspaces are optimized for write access. ENABLE DELTA creates a dbspace named ES_DELTA of size MIN (DELTA_MEMORY_MB, size of ES_USER dbspace) to use row-level versioning in your extended storage. You may add files to ES_DELTA later as needed.

```sql
<enable_delta_clause> ::=  {ENABLE | DISABLE}  DELTA
```

#### add_dbfile_clause

Add one or more dbspace files into specified dbspace.

```sql
<add_dbfile_clause> ::= ALTER DBSPACE <dbspace_name> ADD <new_file_spec> [,
<new_file_spec> ...]
```

##### dbspace_name

Name of the dbspace.

```sql
<dbspace_name> ::= <identifier>
```

##### new_file_spec

Name of the new dbfile.

```sql
<new_file_spec> ::= FILE <logical_filename> 'file-path' <file_opts>
```

##### logical_filename

Logical undelimited name of the dbfile.

```sql
<logical_filename> ::= <identifier>
```

##### file_opts

Options of the dbfile.

```sql
<file_opts> ::= [[SIZE] <file_size> {KB|MB|GB|TB}
   [RESERVE <reserve_size> {KB|MB|GB|TB}]]
```

##### file_size

Size of the dbfile. The size of any individual dbfile added to a dynamic tiering database cannot exceed 1 TB.

```sql
<file_size> ::= <unsigned_integer>
```

##### reserve_size

Reserved size of the dbfile. You can use the reserved space of a dbfile to increase its size.

```sql
<reserve_size> ::= <unsigned_integer>
```

Default values are:

- MB is the default unit for file_size and reserve_size.
- The default value for file_size is 8 MB.
- The default value for reserve_size is 0 MB.

#### empty_dbfile_clause

Empty one or more files from specified dbspace. You must empty files before you can drop them. You can only empty one file per statement.

```sql
<empty_dbfile_clause> ::= ALTER DBSPACE <dbspace_name> EMPTY <empty_file_spec>
```

##### empty_file_spec

Name of the dbfile being emptied.

```sql
<empty_file_spec> ::= FILE <logical_filename>
```

#### drop_dbfile_clause

Drop one or more dbfiles from specified dbspace.

```sql
<drop_dbfile_clause> ::= ALTER DBSPACE <dbspace_name> DROP <drop_file_spec>
[, <drop_file_spec> ...]
```

##### drop_file_spec

Name of the dbfile being dropped.

```sql
<drop_file_spec> ::= FILE <logical_filename>
```

#### increase_dbfile_size_clause

Increase the size of a dbfile for the specified dbspace. The ALTER FILE ADD clause uses dbfile reserved space to enlarge the file. Make sure that there is adequate reserved space before issuing this statement.

```sql
<increase_dbfile_size_clause> ::= ALTER DBSPACE <dbspace_name> ALTER FILE
<logical_filename>
   ADD <add_file_size> {KB|MB|GB|TB}
```

##### add_file_size

New size of the dbfile.

```sql
<add_file_size> ::= <unsigned_integer>
```

## Permissions

You must have the EXTENDED STORAGE ADMIN privilege.

## Description

The ALTER EXTENDED STORAGE statement lets you manage the extended storage space.

## Example

You add a delta dbspace called ES_DELTA to extended storage.

```sql
ALTER EXTENDED STORAGE ENABLE DELTA.
```

You add one or more new dbfiles into dbspace ES_USER.

```sql
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER ADD FILE f1 'f1_file'
   SIZE 100 MB;
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER ADD FILE f2 'f2_file.db' SIZE 200
MB,
   FILE f3 'f3_file.dat' SIZE 100 MB RESERVE 50 MB;
```

You empty and drop one or more dbfiles from dbspace ES_USER.

```sql
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER EMPTY FILE f1;
```

```sql
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER EMPTY FILE f2;
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER EMPTY FILE f3;
```

```sql
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER EMPTY FILE f4;
```

```sql
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER DROP FILE f1, FILE f2, FILE f3,
FILE f4;
```

You increase the size of dbfile f4. This statement uses 10MB from the dbfile reserved space to increase the dbfile size.

```sql
ALTER EXTENDED STORAGE ALTER DBSPACE ES_USER ALTER FILE f4 ADD 10 MB;
```
