# 6.1.35 CLIENTSIDE_ENCRYPTION_COLUMN_KEYS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1439–1441

Provides column encryption key information.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema. |
| COLUMN_KEY_NAME | NVARCHAR(256) | Displays the name of the column encryption key. |
| COLUMN_KEY_ID | VARCHAR(32) | Displays the UUID of the key. |
| ENCRYPTED_WITH_KEYPAIR_ID | VARCHAR(32) | Displays the UUID of the public key that this key is encrypted with. |
| ENCRYPTED_COLUMN_KEYVALUE | VARBINARY(1024) | Displays the value of the key encrypted with the public key referenced by the ENCRYPTED_WITH_KEYPAIR_ID column. |
| ENCRYPTION_ALGORITHM | VARCHAR(16) | Displays the algorithm that this key uses to encrypt data. Possible values: AES-256-CBC and ARIA-256-CBC. |
| CREATE_TIME | TIMESTAMP | Displays the time that the key was created. |
| CREATOR | NVARCHAR(256) | Displays the name of the user who created this key. |
| CREATED_FOR_COLUMN_KEY_ADMIN | VARCHAR(5) | Displays whether created for administrator key copy: TRUE/FALSE. |
| COLUMN_KEY_VERSION | INTEGER | Displays the version of the column encryption key. |
| ALTER_TABLE_IN_PROGRESS | VARCHAR(5) | Displays whether an ALTER TABLE operation is in process using the CEK: TRUE/FALSE. |

## Additional Information

You must have the CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege to access this view.

## Related Information

CLIENTSIDE_ENCRYPTION_KEYPAIRS System View [→](CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) ALTER CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) CREATE CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md) DROP CLIENTSIDE ENCRYPTION KEYPAIR Statement (Encryption) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-CLIENTSIDE-ENCRYPTION-KEYPAIR-Statement-Encryption.md)
