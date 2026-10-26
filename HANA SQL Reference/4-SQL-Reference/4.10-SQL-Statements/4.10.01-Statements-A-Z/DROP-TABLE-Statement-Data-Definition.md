# 4.10.1.107 DROP TABLE Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 925–927

Removes a physical or virtual table from the database.

## Syntax

```sql
DROP TABLE <table_name> [<drop_option>] [ WITH REMOTE ]
```

## Syntax Elements

#### table_name

Drops the specified table or collection table, with the optional schema name.

```sql
<table_name> ::= [ [ <database_name>.]<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the table and dependent objects. RESTRICT drops the table only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

If `<drop_option>` is not specified, then a non-cascaded drop is performed which only drops the specified table. Dependent objects of the table are invalidated but not dropped.

The invalidated objects can be re-validated when an object that has same schema and object name is created. **WITH REMOTE** Drops the virtual table from the local source and the corresponding table on the remote source. This option is only supported for virtual tables. The WITH REMOTE option is supported for remote sources using the following SDA adapters: hanaodbc, iqodbc, aseodbc, tdodbc, voraodbc, odbc (Oracle, Microsoft SQL Server, IBM Netezza, IBM DB2, BigQuery, PostgreSQL). It is not supported with an SDI adapter.

## Description

The DROP TABLE statement removes a physical or virtual table from the database.

## Permissions

This statement requires the DROP object privilege on the table.

Use of the WITH REMOTE option also requires the REMOTE TABLE ADMIN object privilege.

When using the WITH REMOTE option, if the credential type of the remote source is PASSWORD, then only the owner of the remote sources who set the technical user credentials has the authorization to use the option. For all other credential types, authorization is a function of the privileges of the user on the remote source.

## Example

Drop table A and all its dependent objects.

```sql
DROP TABLE A;
```

## Related Information

TABLES System View [→](../../../6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) TABLE_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md)
