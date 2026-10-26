# 4.10.1.112 DROP VIEW Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 933–934

Removes a view from the database.

## Syntax

```sql
DROP VIEW <view_name> [<drop_option>]
```

## Syntax Elements

#### view_name

Drops the specified view, with the optional schema name.

```sql
<view_name> ::= [ <schema_name>. ]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the view and dependent objects. RESTRICT drops the view only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

If `<drop_option>` is not specified, then a non-cascaded drop is performed which only drops the specified view. Dependent objects of the view are invalidated but not dropped.

The invalidated objects can be re-validated when an object that has same schema and object name is created.

## Description

The DROP VIEW statement removes a view from the database.

Dropping a view also drops any expression macros defined for the view. The list of all expression macros for a view can be obtained by querying the VIEW_EXPRESSION_MACROS system view.

## Example

Create table t, and then a view, v, that selects all records from table t.

```sql
CREATE ROW TABLE t (a INT);
 CREATE VIEW v AS SELECT * FROM t;
```

Drop view v from the database.

```sql
DROP VIEW v;
```

## Related Information

[VIEW_EXPRESSION_MACROS System View](../../../6-System-Views-Reference/6.01-System-Views/VIEW_EXPRESSION_MACROS-System-View.md)
