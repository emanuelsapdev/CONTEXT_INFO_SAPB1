# 4.10.1.2 ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 419–421

Alters a column encryption key (CEK) to grant or remove access to it, populate it with encryption key information, and add or drop versions of the CEK.

## Syntax

```sql
ALTER CLIENTSIDE ENCRYPTION COLUMN KEY [ <schema_name>.]<key_name>
 [ { ADD | DROP } KEYCOPY ] ENCRYPTED WITH KEYPAIR <keypair_name>
 | ADD NEW VERSION
 | DROP OLD VERSIONS
```

## Syntax Elements

#### schema_name

Specifies the schema name for the CEK.

```sql
<schema_name> ::= <identifier>
```

#### key_name

Specifies the name of the CEK to alter.

#### { ADD | DROP } KEYCOPY

Specifies to create (ADD) or drop a key copy of the CEK.

#### ENCRYPTED WITH KEYPAIR keypair_name

Specifies the name of the client key pair (CKP) to use for encrypting the column key.

```sql
<keypair_name> ::= <identifier>
```

**ADD NEW VERSION** Creates a new version of the encryption key. **DROP OLD VERSIONS** Removes all old versions of the encryption key. Encrypted columns that are using the old version(s) of the CEK must be re-encrypted using the new version of the CEK before the old version can be dropped.

## Description

When a column encryption key is created by the key administrator (user with CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege), no other user will have access to this CEK and there is only one encrypted value for the CEK. When a particular client installation requires access to a CEK, the client creates a client key pair using the CREATE CLIENTSIDE ENCRYPTION KEYPAIR`<keypair_name>` syntax. When the key administrator uses the ADD KEYCOPY clause, the client driver collaborates with the SAP HANA server to create a copy of the CEK that is encrypted with the key pair name specified in the statement (ENCRYPTED WITH KEYPAIR `<keypair_name>`) and created previously by the client. The key value of the CEK copy is added to the SAP HANA database, thus granting access to the CEK and the data encrypted with this CEK to the client installation.

With DROP KEYCOPY, access to the CEK is removed from the SAP HANA database. If the key copy being dropped belongs to the key administrator, then the SAP HANA server ensures that at least one other key administrator key copy (CEK copy encrypted by a CKP owned by the key administrator) exists for that CEK. If no other key administrator key copies exist for that CEK, then DROP KEYCOPY fails. This behavior ensures that the key administrator can create key copies for the CEK that grants access to encrypted data.

When an empty CEK is created using a CREATE CLIENTSIDE ENCRYPTION COLUMN KEY...HEADER ONLY statement, there is no encrypted value for the CEK in the SAP HANA database. An empty CEK allows the client to proceed with database schema creation without actually creating the CEK. With the ENCRYPTED WITH KEYPAIR `<keypair_name>` syntax, the client driver collaborates with the SAP HANA server to generate a new CEK and encrypts it with `<keypair_name>`, which is then stored in the SAP HANA database. Once the empty CEK is populated, rows can be inserted into the table. The {ADD | DROP} KEYCOPY clause is not used to populate the empty CEK.

The ADD VERSION clause creates a new version of an existing CEK. The ALTER TABLE `<activate_clientside_encryption>` clause then applies the new CEK version to the encrypted column.

## Permissions

This statement requires the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege.

## Examples

The following statement creates a key copy of the CEK `hrapp_cek1` for user key pair `user1_ckp`. This statement allows user1 to access CEK `hrapp_cek1` and thus the encrypted column that the CEK encrypts.

```sql
ALTER CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek1 ADD KEYCOPY ENCRYPTED WITH
KEYPAIR user1_ckp;
```

The following statement drops the key copy of CEK `hrapp_cek1` encrypted with key pair `user1_ckp`. This statement prevents the client from having access to `hrapp_cek1` through the client key pair `user1_ckp`.

```sql
ALTER CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek1 DROP KEYCOPY ENCRYPTED WITH
KEYPAIR user1_ckp;
```

The following statement alters an empty CEK `hrapp_cek2` (defined as HEADER ONLY) and encrypts with `user1_ckp`.

```sql
CREATE CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek2 HEADER ONLY;
ALTER CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek2 ENCRYPTED WITH KEYPAIR
user1_ckp;
```

The following statement adds a new version of the existing CEK hrapp_cek3.

```sql
ALTER CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek2 ADD NEW VERSION;
```

The following statement drops an old version of the existing CEK hrapp_cek3.

```sql
ALTER CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek2 DROP OLD VERSIONS;
```

## Related Information

CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) CLIENTSIDE_ENCRYPTION_KEYPAIRS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) ALTER TABLE Statement (Data Definition) [→](4.10.01.20-ALTER-TABLE/README.md)
