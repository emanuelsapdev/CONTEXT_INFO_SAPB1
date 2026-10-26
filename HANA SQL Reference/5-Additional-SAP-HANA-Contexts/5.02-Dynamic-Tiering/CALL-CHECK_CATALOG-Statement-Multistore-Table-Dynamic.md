# 5.2.11 CALL CHECK_CATALOG Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1264–1267

Performs consistency checks of metadata in both multistore and extended store tables, based on the actions you specify as arguments to the procedure call.

## Syntax

```sql
CALL CHECK_CATALOG ('<action>', '<schema_name>', '<object_name>',
'<catalog_object_type>')
```

## Syntax Elements

**action** The type of consistency check to perform.

```sql
<action> ::=
 CHECK_ES_METADATA
 | REPAIR_ES_METADATA
 | CHECK
 | CHECK_VALUE_DOMAIN
 | CHECK_OBJECT_REFERENTIAL_INTEGRITY
```

##### CHECK_ES_METADATA

Checks the metadata of a multistore or extended store table for inconsistencies such as missing tables, columns, and indexes.

##### REPAIR_ES_METADATA

Fixes metadata inconsistencies by deleting orphaned objects found by running CHECK_ES_METADATA.

##### CHECK

Performs all available checks. When you perform this action on a multistore table, it is only applied to the column store partitions of the multistore table; checks are not performed on extended storage partitions.

##### CHECK_VALUE_DOMAIN

Checks the consistency of value domains in the catalog object (such as table type, field types, and so on). When you perform this action on a multistore table, it is only applied to the column store partitions of the multistore table; checks are not performed on extended storage partitions.

##### CHECK_OBJECT_REFERENTIAL_INTEGRITY

Checks the consistency of references in the catalog object. When you perform this action on a multistore table, it is only applied to the column store partitions of the multistore table; checks are not performed on extended storage partitions.

#### schema_name

Specifies the name of the analyzed schema.

#### object_name

Specifies the name of the analyzed object. **catalog_object_type** Specifies the type of object to analyze.

```sql
<catalog_object_type> ::=
 TABLE
 | INDEX
 | COLUMN
 | NULL
```

Use NULL to check for all extended storage objects.

## Permissions

The privilege needed depends on the clause used:

- Check action – CATALOG READ or DATA ADMIN
- Repair action – DATA ADMIN

## Description

The CALL CHECK_CATALOG statement performs a variety of consistency checks in both multistore and extended store tables, depending on the actions you specify as arguments to the procedure call.

CHECK_CATALOG only checks the metadata of objects, and does not check the actual structure or data of tables and indexes.

Use `<schema_name>`, `<object_name>`, and `<catalog_object_type>` to define specific schemas or objects to check. Otherwise, enter NULL as the value for these parameters to check all objects in all schemas.

See the following:

- SAP HANA SQL and System Views Reference > SQL Reference > SQL Statements > Procedural Statements > CALL Statement (Procedural)
- SAP HANA Administration Guide > System Administration> Table and Catalog Consistency Checks > Catalog Consistency Check
- SAP Note 1977584 – Technical Consistency Checks for SAP HANA Databases

## Example

You call this procedure to perform a consistency check of the `tab1` table in the MYSCHEMA schema in the extended store and multistore table:

> **Sample Code**
>
> ```sql
> CALL CHECK_CATALOG ('CHECK_ES_METADATA', 'MYSCHEMA', 'tab1', 'table');
> ```

> **Output Code**
>
> ```sql
> SCHEMA,NAME,OBJECT_TYPE,ERROR_CODE,ERROR_MESSAGE
> MYSCHEMA, TAB1, table , -301 , 'orphan table in extended storage'
> ```

The output is empty if there is no inconsistency.

## Related Information

SAP Note 1977584
