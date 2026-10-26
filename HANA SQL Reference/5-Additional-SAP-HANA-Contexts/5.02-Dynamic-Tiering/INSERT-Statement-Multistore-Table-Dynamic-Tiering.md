# 5.2.34 INSERT Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1356–1359

## Syntax

```sql
INSERT INTO <table_name> [ <column_list_clause> ] { <value_list_clause>
  | <subquery> }
```

## Syntax Elements

#### table_name

The table where the insert is to be performed, with optional schema name.

```sql
<table_name> ::= [ <schema_name>. ]<identifier>
<schema_name> ::= <unicode_name>
```

#### column_list_clause

A list of column identifiers, ordered in the order of values in the `<value_list_clause>` or `<subquery>`.

```sql
 <column_list_clause> ::= ( <column_name>, ... )
<column_name> ::= <identifier>
```

If the column list is omitted, the database performs the insert using all the columns in the table. A column omitted from the column list will be filled using the column default value. For more information on identifiers, see the Introduction in the SAP HANA SQL and System Views Reference.

#### value_list_clause

A list of values, or expressions evaluating to values, that will be inserted into the table.

```sql
<value_list_clause> ::= VALUES ( <expression>, ... )
```

For descriptions of expressions, see Expressions in the SAP HANA SQL and System Views Reference.

#### subquery

For more information about subqueries, see the SELECT in the SAP HANA SQL and System Views Reference.

```sql
<subquery>
```

#### hint_clause

For more information about hints, see SELECT in the SAP HANA SQL and System Views Reference.

```sql
<hint_clause>
```

## Permissions

You must have the INSERT object privilege.

## Description

The INSERT statement adds a record to a multistore table. The values to be inserted can either be values, expressions or the result of a subquery. If the subquery used does not return any records, then the database will not insert any records into the table.

Multistore tables do not support `<hint_clause>`. They do support:

- Single row inserts
- Array inserts using parameters
- INSERT SELECT statements

You should always define the `<column_list_clause>`. This helps to protect your INSERT queries from damaging data if the target table schema is modified.

## Example

You create table T:

```sql
CREATE COLUMN TABLE T (VAL1 INT, VAL2 INT, VAL3 DATE, PRIMARY KEY (VAL1, VAL2))
PARTITION BY RANGE (VAL1)
( partition 10 <= values < 20 , partition 20 <=values < 30 )
, RANGE (val2)
    ( USING DEFAULT STORAGE ( PARTITION 10 <=VALUES < 20, PARTITION 20 <= VALUES
< 30 )
      USING EXTENDED STORAGE ( PARTITION 30 <=VALUES < 50, PARTITION 50 <=VALUES
< 100 ))
```

You insert a row into table T.

```sql
INSERT INTO T VALUES (11, 11, '20160101');
```

| VAL1 | VAL2 | VAL3 |
| --- | --- | --- |
| 11 | 11 | Jan 1, 2016 |

You insert a new row into table T using column list to specify which columns should receive the input values.

```sql
INSERT INTO T (VAL1, VAL2) VALUES (12,13);
```

| VAL1 | VAL2 | VAL3 |
| --- | --- | --- |
| 11 | 12 | ? |

You insert a row into table T using a subquery.

```sql
INSERT INTO T SELECT 12, 12, '20160101' FROM DUMMY;
```

| VAL1 | VAL2 | VAL3 |
| --- | --- | --- |
| 12 | 12 | January 1, 2016 |
