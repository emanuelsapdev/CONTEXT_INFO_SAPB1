# 4.10.1.103 DROP SEQUENCE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 918–919

Removes a sequence.

## Syntax

```sql
DROP SEQUENCE <sequence_name> [<drop_option>]
```

## Syntax Elements

#### sequence_name

Drops the specified sequence, with the optional schema name.

```sql
<sequence_name> ::= [<schema_name>.]<identifier>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the sequence and dependent objects. RESTRICT drops the sequence only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

If `<drop_option>` is not specified, then a non-cascaded drop is performed, which only drops the specified sequence. Dependent objects of the sequence are invalidated but not dropped.

## Description

The DROP SEQUENCE statement removes a sequence.

Invalidated objects can be re-validated when an object that has same schema and object name is created.

## Example

Create a sequence named seq.

```sql
CREATE SEQUENCE seq START WITH 11;
```

Drop the sequence named seq.

```sql
DROP SEQUENCE seq;
```
