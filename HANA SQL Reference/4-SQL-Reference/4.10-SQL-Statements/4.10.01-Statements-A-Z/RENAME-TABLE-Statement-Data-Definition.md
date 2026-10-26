# 4.10.1.138 RENAME TABLE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1026–1028

Changes the schema and/or the name of a table.

## Syntax

```sql
RENAME TABLE <current_table_name> TO <new_table_name>
```

## Syntax Elements

#### current_table_name

Specifies the current name of the table, with optional schema name.

```sql
<current_table_name> ::= [<schema_name>.]<identifier>
```

#### new_table_name

Specifies a new table name and/or schema for `<current_table_name>`.

```sql
<new_table_name> ::= [<schema_name>.]<identifier>
```

If a table with the same name as `<new_table_name>` already exists in `<schema_name>`, or if `<schema_name>` doesn't exist, an error is returned.

## Description

The RENAME TABLE statement changes the schema and/or the name of a table.

## Example

### Example 1 - Renaming a table in the current schema

Create table A in the current schema.

```sql
CREATE COLUMN TABLE A (A INT PRIMARY KEY, B INT);
```

Show a list of table names in the current schema.

```sql
SELECT TABLE_NAME FROM TABLES WHERE SCHEMA_NAME = CURRENT_SCHEMA ORDER BY
TABLE_NAME;
```

| **TABLE_NAME** |
| --- |
| A |
| ... |

Rename table A to a new name B.

```sql
RENAME TABLE A TO B;
```

Show a list of table names in current schema after the renaming process.

```sql
SELECT TABLE_NAME FROM TABLES WHERE SCHEMA_NAME = CURRENT_SCHEMA ORDER BY
TABLE_NAME;
```

| **TABLE_NAME** |
| --- |
| B |
| ... |

### Example 2 - Renaming a table in another schema

Create schema mySchema and then create a table A in the new schema.

```sql
CREATE SCHEMA mySchema;
CREATE COLUMN TABLE mySchema.A (A INT PRIMARY KEY, B INT);
```

Show the list of table names in schema mySchema.

```sql
SELECT TABLE_NAME FROM TABLES WHERE SCHEMA_NAME = 'MYSCHEMA' ORDER BY TABLE_NAME;
```

| **TABLE_NAME** |
| --- |
| A |

Rename table A in mySchema to B.

```sql
RENAME TABLE mySchema.A TO B;
```

Show a list of table names in schema mySchema after the renaming process.

```sql
SELECT TABLE_NAME FROM TABLES WHERE SCHEMA_NAME = 'MYSCHEMA' ORDER BY TABLE_NAME;
```

| **TABLE_NAME** |
| --- |
| B |

### Example 3 - Change the schema of the table

Create schema mySchema2.

```sql
CREATE SCHEMA mySchema2;
```

Change the schema of table B from mySchema to mySchema2.

```sql
RENAME TABLE mySchema.B TO mySchema2.B;
```

Show a list of table names in the schema mySchema2.

```sql
SELECT TABLE_NAME FROM TABLES WHERE SCHEMA_NAME = 'MYSCHEMA2' ORDER BY
TABLE_NAME;
```

| **TABLE_NAME** |
| --- |
| B |
