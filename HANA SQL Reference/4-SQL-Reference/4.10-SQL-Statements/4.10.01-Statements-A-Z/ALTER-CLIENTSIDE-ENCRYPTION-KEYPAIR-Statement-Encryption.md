# 4.10.1.3 ALTER CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 421–423

Adds a new version of a client-side encryption key pair (CKP), or drops all older versions of a CKP.

## Syntax

```sql
ALTER CLIENTSIDE ENCRYPTION KEYPAIR <keypair_name> <add_drop_version>
```

## Syntax Elements

#### keypair_name

Specifies the name of an existing CKP.

#### add_drop_versions

Adds a new version of the specified CKP, or drops all previous versions.

```sql
<add_drop_versions> ::= { ADD NEW VERSION | DROP OLD VERSIONS }
```

## Description

The client-driver uses this statement to create a new version of an existing CKP which the SAP HANA server then stores in the catalog, or to delete all older versions of a CKP.

Dropping of old versions of CKP also drops the key copies of the CEK that they encrypt.

Dropping old versions fails if any of the older versions of CKP encrypts the last key copy of a CEK version

If all key copies of CEK encrypted by older versions of CKP are encrypted with latest version of CKP which belongs to the key admin, then older versions of CKP are dropped along with the key copies of CEK that they encrypt.

## Permissions

To add a new version, you must be the owner of the CKP and have ALTER CLIENTSIDE ENCRYPTION KEYPAIR privilege. To drop old versions, you must have the ALTER CLIENTSIDE ENCRYPTION KEYPAIR privilege

## Examples

The following example creates a CKP, `Ckp1`, creates a new version of it, and then drops all old versions of it.

```sql
CREATE CLIENTSIDE ENCRYPTION KEYPAIR Ckp1 ALGORITHM 'RSA-OAEP-2048';
ALTER CLIENTSIDE ENCRYPTION KEYPAIR Ckp1 ADD NEW VERSION;
ALTER CLIENTSIDE ENCRYPTION KEYPAIR Ckp1 DROP OLD VERSIONS;
```

## Related Information

CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) CLIENTSIDE_ENCRYPTION_KEYPAIRS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md)
