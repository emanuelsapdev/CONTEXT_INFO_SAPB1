# 5.2.16 CREATE EXTENDED STORAGE Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1279–1281

Creates a new extended storage database, starts it, and registers it as an SAP HANA service.

## Syntax

```sql
CREATE EXTENDED STORAGE [ AT [LOCATION] '<host-string>' ] SIZE <size-value> {KB|
MB|GB|TB} [{ENABLE|DISABLE} DELTA]
```

## Syntax Elements

#### host-string

Specifies the host on which extended storage is being created. The host name must exactly match the host name that appears in the M_SERVICES view.

```sql
<host-string> ::= <string_literal>
```

#### size-value

Specifies the size of data to be managed in extended storage. Initial size cannot exceed 1 TB. The size of any individual dbfile added to a dynamic tiering database cannot exceed 1 TB.

```sql
<size-value> ::= <int_literal>
```

#### ENABLE | DISABLE DELTA

Specifies whether RLV store is created on extended storage. ENABLE DELTA supports row-level versioning. The default is DISABLE DELTA (table-level versioning).

```sql
ENABLE | DISABLE DELTA
```

## Permissions

You must have the EXTENDED STORAGE ADMIN privilege.

## Description

The CREATE EXTENDED STORAGE statement creates a new extended storage database, starts it, and registers it as an SAP HANA service.

> **Note**
>
> If you create extended storage, you cannot then enable data volume encryption in the SAP HANA database. You can, however, first enable data volume encryption in the SAP HANA database before creating extended storage. Alternatively, you can convert an existing unencrypted SAP HANA database with extended storage by performing a backup and restore. See Extended Storage Database Encryption in the SAP HANA Dynamic Tiering: Administration Guide for more information.

> **Caution**
>
> Creating extended storage after a full data backup, but before recovery, will break business continuity. See 2375865 .

## Example

This creates an extended storage of size 10 GB on host `dbhost.example.com` with delta capability enabled.

```sql
CREATE EXTENDED STORAGE AT 'dbhost.example.com' size 10 GB ENABLE DELTA
```
