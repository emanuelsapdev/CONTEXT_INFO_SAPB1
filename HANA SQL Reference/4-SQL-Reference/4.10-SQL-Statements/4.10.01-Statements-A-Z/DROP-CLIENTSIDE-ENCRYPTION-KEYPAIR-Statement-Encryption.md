# 4.10.1.85 DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 897–898

Drops a client key pair (CKP).

## Syntax

```sql
DROP CLIENTSIDE ENCRYPTION KEYPAIR <keypair_name>
```

## Syntax Elements

#### keypair_name

Specifies the name of the CKP.

## Description

Executing this statement removes the specified CKP from the catalog along with every column encryption key copy assigned to it. The client driver and the SAP HANA server collaborate transparently to remove this key pair from the client hdbkeystore.

The SAP HANA server ensures that at least one other key administrator key copy (CEK copy encrypted by CKP of user with CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege) exists for the column encryption key being dropped. If there are no key administrator key copies, then the statement fails.

## Permissions

Users can drop key pairs they created. However, this statement requires the DROP CLIENTSIDE ENCRYPTION KEYPAIR privilege to drop key pairs that were created by other users.

## Examples

The following example drops the client key pair `user1_ckp`:

```sql
DROP CLIENTSIDE ENCRYPTION KEYPAIR user1_ckp;
```

## Related Information

CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) CLIENTSIDE_ENCRYPTION_KEYPAIRS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md)
