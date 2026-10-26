# 4.10.1.108 DROP TRIGGER Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 927–928

Deletes a trigger.

## Syntax

```sql
DROP TRIGGER <trigger_name> [ <drop_option> ] [ ONLINE ]
```

## Syntax Elements

#### trigger_name

Drops the specified trigger, with the optional schema name.

```sql
<trigger_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the trigger and dependent objects. RESTRICT drops the trigger only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

If `<drop_option>` is not specified, then a non-cascaded drop is performed, which only drops the specified trigger. Dependent objects of the trigger are invalidated but not dropped.

#### ONLINE

Applies an intentional exclusive lock (instead of an exclusive lock) before performing the operation. An intentional exclusive lock differs from the default lock (exclusive) because it allows concurrent DML and DDL related to the object to proceed, and will retry the operation until it can proceed.

ONLINE applies an intentional exclusive lock only if the auto commit mode for DDL statements is set to on. If the auto commit mode for DDL statement is not set to on, then an exclusive lock is still applied.

## Description

Invalidated objects can be re-validated when an object that has same schema and object name is created.

## Permissions

Only database users with the TRIGGER privilege for the table on which the trigger was defined are allowed to drop a trigger for that table.

## Example

Create two tables, `target` and `sample`, and a trigger called `test`.

```sql
CREATE ROW TABLE target ( A INT);
 CREATE ROW TABLE sample ( A INT);
 CREATE TRIGGER test
 AFTER UPDATE ON target
 BEGIN
   INSERT INTO sample VALUES(3);
 END;
```

Drop the trigger called test.

```sql
DROP TRIGGER test;
```

Alternatively, you can drop the trigger and specify ONLINE so that the operation proceeds only when concurrent DML or DDL finishes.

```sql
DROP TRIGGER test ONLINE;
```
