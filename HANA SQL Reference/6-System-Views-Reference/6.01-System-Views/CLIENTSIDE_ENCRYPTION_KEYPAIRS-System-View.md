# 6.1.36 CLIENTSIDE_ENCRYPTION_KEYPAIRS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1441–1442

Provides information about client public keys in the SAP HANA database.

| **Name** | **Type** | **Description** |
| --- | --- | --- |
| KEYPAIR_NAME | NVARCHAR(256) | Displays the name of the client public key. |
| KEYPAIR_ID | VARCHAR(32) | Displays the UUID key identifier. |
| ENCODED_PUBLIC_KEYVALUE | NCLOB | Displays the PEM-encoded x509 value of the key. |
| ENCRYPTION_ALGORITHM | VARCHAR(16) | Displays the algorithm the key uses to encrypt column keys. Possible values are: RSA-OAEP-2048. |
| CREATE_TIME | TIMESTAMP | Displays the time the key was created. |
| CREATOR | NVARCHAR(256) | Displays the name of the user who created the key. |
| KEYPAIR_VERSION | INTEGER | Displays the version of the key. |

## Related Information

CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View [→](CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md)
