# 4.9.1.154 RECORD_COMMIT_TIMESTAMP Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 288–290

Returns a COMMIT timestamp for the specified row of the given table.

## Syntax

```sql
RECORD_COMMIT_TIMESTAMP(<table_name_or_alias>)
```

## Syntax Elements

**table-name-or-alias** Specifies the name or alias of the table to return the COMMIT timestamps for.

## Description

Returns a COMMIT timestamp for the specified row of the given table if the table is tracking COMMIT timestamps for each row. The COMMIT timestamp is based on an internal counter that increases on commit operations and does not contain a date or time. If the table is not tracking COMMIT timestamps, the function returns NULL.

Depending on the table type, DDL statements such as ALTER TABLE can affect the value returned by the RECORD_COMMIT_TIMESTAMP function:

- For column store tables, the returned value is not affected by DDL operations.
- For row store tables, the returned value is changed to the COMMIT timestamp of the transaction that performed the DDL operation.

## Example

Execute the following statements to create and populate two tables, AA and BB, where AA records COMMIT timestamps and BB does not.

```sql
CREATE TABLE AA (A int) RECORD COMMIT TIMESTAMP;
CREATE TABLE BB (B int);
INSERT INTO AA VALUES (1);
INSERT INTO BB VALUES (1);
COMMIT;
```

Assume the transaction is committed with a COMMIT timestamp of 10. Executing the following statement returns the COMMIT timestamp of the transaction, in this case, 10.

```sql
SELECT RECORD_COMMIT_TIMESTAMP(AA) FROM AA;
```

Executing a similar statement on table BB returns NULL since the RECORD COMMIT TIMESTAMP option was not set for table BB.

```sql
SELECT RECORD_COMMIT_TIMESTAMP(BB) FROM BB;
```
