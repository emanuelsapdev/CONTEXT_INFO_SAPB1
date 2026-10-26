# 4.10.1.40 COMMENT ON Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 680–682

Adds a comment to an object in the database, or removes an existing comment.

## Syntax

```sql
COMMENT ON <object_type> <object_name> IS <comment>
```

## Syntax Elements

#### object_type

Specifies the type of object to add the comment on.

```sql
<object_type> ::=
 TABLE
 | VIEW
 | COLUMN
 | USER
 | ROLE
 | USERGROUP
```

#### object_name

Specifies the name of the object to add a commented on, with optional schema name.

```sql
<object_name> ::= [<schema_name>.]<identifier>
```

#### comment

Specifies the comment for the object.

```sql
<comment> ::= <string_literal> | NULL
```

If NULL is specified, then any existing comment is dropped.

## Description

Comments are a useful way to record an intuitive description of objects in the database such as tables, columns, and users. You can also remove comments.

## Examples

#### Comment on a table

Create a table and add a comment on it.

```sql
CREATE ROW TABLE COMMENT_ON_EX(A INT);
 COMMENT ON TABLE COMMENT_ON_EX IS 'Used for comment on examples';
```

Select the table from the TABLES system table to view the comment.

```sql
SELECT * FROM TABLES WHERE table_name='COMMENT_ON_EX';
```

#### Comment on a table column

Comment on column A of the COMMENT_ON_EX table from example 1.

```sql
COMMENT ON COLUMN COMMENT_ON_EX.A IS 'This is an example column comment';
```

Select the column description from the TABLE_COLUMNS system table.

```sql
SELECT * FROM TABLE_COLUMNS WHERE table_name='COMMENT_ON_EX';
```

#### Comment on a view and view column

Create a view, a view comment, and view column comment.

```sql
CREATE VIEW COMMENT_ON_EX_VIEW AS SELECT * FROM COMMENT_ON_EX;
 COMMENT ON VIEW COMMENT_ON_EX_VIEW IS 'This is a view comment';
 COMMENT ON COLUMN COMMENT_ON_EX_VIEW.A IS 'This is a view column comment';
```

Select the view comment and view column comments from the relevant system tables.

```sql
SELECT * FROM VIEWS WHERE view_name='COMMENT_ON_EX_VIEW';
 SELECT * FROM VIEW_COLUMNS WHERE view_name='COMMENT_ON_EX_VIEW';
```

#### Remove comments

Drop a view comment and a view column comment.

```sql
COMMENT ON VIEW COMMENT_ON_EX_VIEW IS NULL;
COMMENT ON COLUMN COMMENT_ON_EX_VIEW.A IS NULL;
```

## Related Information

TABLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) VIEWS System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIEWS-System-View.md) VIEW_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/VIEW_COLUMNS-System-View.md)
