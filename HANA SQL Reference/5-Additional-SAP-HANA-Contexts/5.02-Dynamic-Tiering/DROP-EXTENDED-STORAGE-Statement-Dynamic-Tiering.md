# 5.2.23 DROP EXTENDED STORAGE Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1316–1317

Removes an existing extended storage configuration from the SAP HANA database.

## Syntax

```sql
DROP EXTENDED STORAGE [<drop_option>]
```

## Syntax Elements

#### drop_option

When `<drop_option>` is not specified a restrict drop is performed.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

##### CASCADE

Drops the extended storage and dependent objects.

##### RESTRICT

Drops the extended storage only when dependent objects do not exist. If this drop option is used and a dependent object exists an error is thrown.

## Permissions

You must have the EXTENDED STORAGE ADMIN privilege.

## Description

The DROP EXTENDED STORAGE statement removes an existing extended storage configuration from the SAP HANA database.

Dropping extended storage drops all dynamic tiering partitions for multistore.

> **Caution**
>
> Dropping extended storage after a full data backup, but before recovery, will break business continuity. See SAP Note 2375865 – Backup and Recovery Functional Restrictions.

## Example

This drops an extended storage if there are no dependent objects like extended tables.

```sql
DROP EXTENDED STORAGE
```

The above example drops extended storage with all dependent objects like extended tables.

```sql
DROP EXTENDED STORAGE CASCADE
```
