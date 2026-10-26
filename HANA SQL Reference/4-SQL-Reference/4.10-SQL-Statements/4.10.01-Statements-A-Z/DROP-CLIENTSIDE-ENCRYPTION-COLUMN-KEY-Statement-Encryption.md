# 4.10.1.84 DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 896–897

Drops a column encryption key (CEK) and any key copies for it from the schema.

## Syntax

```sql
DROP CLIENTSIDE ENCRYPTION COLUMN KEY [ <schema>.]<key_name>
```

## Syntax Elements

#### schema_name

Specifies the schema name.

```sql
<schema_name> ::= <unicode_name>
```

#### key_name

Specifies the name of the CEK to drop.

## Description

When you execute this statement, the CEK and all its key copies are dropped from the catalog.

If there are columns encrypted with the CEK, then the operation fails and nothing is dropped. All columns using the column encryption key must first be dropped or must stop using the CEK.

## Permissions

This statement requires the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege.

## Examples

The following statement drops the column encryption key `<hrapp_cek1>`:

```sql
DROP CLIENTSIDE ENCRYPTION COLUMN KEY mychema.hrapp_cek1;
```

## Related Information

CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) CLIENTSIDE_ENCRYPTION_KEYPAIRS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md)
