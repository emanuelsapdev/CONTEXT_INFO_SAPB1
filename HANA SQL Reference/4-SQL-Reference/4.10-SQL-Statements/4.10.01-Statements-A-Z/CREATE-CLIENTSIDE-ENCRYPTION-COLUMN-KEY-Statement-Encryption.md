# 4.10.1.45 CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 700–702

Creates a column encryption key (CEK) to be used in client-side encryption.

## Syntax

```sql
CREATE CLIENTSIDE ENCRYPTION COLUMN KEY [ <schema_name>.]<key_name>
   [ ALGORITHM <algorithm_name> ]
   { ENCRYPTED WITH KEYPAIR <keypair_name> | HEADER ONLY }
```

## Syntax Elements

#### schema_name

Specifies the schema name for the CEK.

```sql
<schema_name> ::= <identifier>
```

#### key_name

Specifies the name of the CEK.

```sql
<key_name> ::= <identifier>
```

#### ALGORITHM algorithm_name

Specifies the algorithm to use for encryption of columns. Currently, only AES-256-CBC (default) and ARIA-256-CBC are supported.

```sql
<algorithm_name> ::= '<string>'
```

#### ENCRYPTED WITH KEYPAIR keypair_name

Specifies the name of the client key pair (CKP) to use for encrypting the column key.

```sql
<keypair_name> ::= <identifier>
```

#### HEADER ONLY

Creates an empty CEK that you can use for schema creation without requiring the creation of actual encryption keys.

## Description

CEKs are symmetric keys used to encrypt sensitive data columns in the client drivers. Creating a CEK is required before any column in the database can be encrypted by using the client-side encryption feature. Before creating an encrypted CEK, you must define a client key pair by using the CREATE CLIENTSIDE ENCRYPTION KEYPAIR statement.

The client can specify a key pair name (`<keypair_name>`) to encrypt the new CEK. The client driver collaborates with the SAP HANA server transparently to generate a new CEK encrypted with the specified public key (`<keypair_name>`). The new CEK is then stored in the SAP HANA database catalog.

Use HEADER ONLY to allow the client to proceed with database schema creation (with client-side encryption) without creating and specifying actual key information during creation. A CREATE TABLE statement may reference an empty CEK. An ALTER TABLE statement on an empty table may also reference an empty CEK. Any attempt to insert rows into the table fails until the CEK has been populated by an ALTER CLIENTSIDE ENCRYPTION COLUMN KEY statement.

## Permissions

Specifying ENCRYPTED WITH KEYPAIR `<keypair_name>` requires the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege. Creating an empty CEK (HEADER ONLY) requires the CREATE ANY or CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege.

## Examples

The following statement creates an column encryption key hrapp_cek1 that uses the AES-256-CBC encryption algorithm, encrypted with key pair key_admin_ckp:

```sql
CREATE CLIENTSIDE ENCRYPTION COLUMN KEY myschema.hrapp_cek1 ALGORITHM 'AES-256-
CBC' ENCRYPTED WITH KEYPAIR key_admin_ckp;
```

The following statement creates an empty column encryption key hrapp_cek2 that uses the AES-256-CBC encryption algorithm:

```sql
CREATE CLIENTSIDE ENCRYPTION COLUMN KEY hrapp_cek2 ALGORITHM 'AES-256-CBC'
HEADER ONLY;
```

## Related Information

CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) CLIENTSIDE_ENCRYPTION_KEYPAIRS System View [→](../../../6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](DROP-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md)
