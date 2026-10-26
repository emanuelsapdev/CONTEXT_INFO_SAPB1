# 4.10.1.19.6 ALTER SYSTEM {ENABLE | DISABLE} STATEMENT HINT Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 476–477

Enables or disables hints from a target query or statement hash.

## Syntax

```sql
ALTER SYSTEM ENABLE STATEMENT HINT FOR { <target_query> | STATEMENT HASH
<statement_hash> | ALL };
| ALTER SYSTEM DISABLE STATEMENT HINT FOR { <target_query> | STATEMENT HASH
<statement_hash> | ALL };
```

## Syntax Elements

#### target_query

Specifies the target query. **statement_hash** Specifies the statement hash. **ALL** Applies the action to both userdefined hints and system hints that are associated with the specified statement. If ALL is not specified, then the action is only applied on the userdefined hints.

## Description

Both statements (ENABLE, DISABLE) evict all cached plans for the target SQL statements from the SQL Plan Cache.

## Example

This example enables all statement hints.

```sql
ALTER SYSTEM ENABLE STATEMENT HINT FOR ALL;
```

This example disables statement hints for the SELECT query.

```sql
ALTER SYSTEM DISABLE STATEMENT HINT FOR SELECT * FROM AAA, BBB WHERE AAA.X =
BBB.X;
```

This example enables statement hints for the statement hash 36896ef08346b8321f88449d5c5e97f8.

```sql
ALTER SYSTEM ENABLE STATEMENT HINT FOR STATEMENT HASH
'36896ef08346b8321f88449d5c5e97f8';
```

This example disables statement hints for the statement hash 36896ef08346b8321f88449d5c5e97f8.

```sql
ALTER SYSTEM DISABLE STATEMENT HINT FOR STATEMENT HASH
'36896ef08346b8321f88449d5c5e97f8';
```

## Related Information

[ALTER SYSTEM {ADD | ALTER | REMOVE} STATEMENT HINT Statement (System Management)](ALTER-SYSTEM-ADD-ALTER-REMOVE-STATEMENT-HINT-Statement.md)
