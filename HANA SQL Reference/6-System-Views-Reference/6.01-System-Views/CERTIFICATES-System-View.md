# 6.1.34 CERTIFICATES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1438–1439

Provides information about certificates useable in PSEs.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CERTIFICATE_ID | BIGINT | Displays the unique identification of the certificate. |
| SUBJECT_COMMON_NAME | NVARCHAR(5000) | Displays the distinguished name of the X.509 certificate subject. |
| ISSUER_COMMON_NAME | NVARCHAR(5000) | Displays the common name of the X. 509 certificate issuer. |
| VALID_FROM | TIMESTAMP | Displays the start time of certificate's validity. |
| VALID_UNTIL | TIMESTAMP | Displays the end time of certificate's validity. |
| COMMENT | NVARCHAR(1024) | Displays the description for the certificate. |
| SUBJECT_DISTINGUISHED_NAME | NVARCHAR(5000) | Displays the distinguished name of the X.509 certificate subject. |
| ISSUER_DISTINGUISHED_NAME | NVARCHAR(5000) | Displays the distinguished name of the X.509 certificate issuer. |
| BASIC_CONSTRAINTS | NVARCHAR(32) | Displays the basic constraints. |
| SUBJECT_ALT_NAME | NVARCHAR(5000) | Displays the comma-separated list of alternative names of the X.509 certificate subject. |
| PUBLIC_KEY_ALGORITHM | NVARCHAR(256) | Displays the public key algorithm. |
| PUBLIC_KEY_LENGTH | SMALLINT | Displays the public key length. |
| KEY_USAGE | NVARCHAR(256) | Displays the comma-separated list of key usage strings as specified in RFC 5280. |
| SIGNATURE_ALGORITHM | NVARCHAR(256) | Displays the signature algorithm. |
| VERSION | TINYINT | Displays the version of the certificate format. |
| SERIAL_NUMBER | NVARCHAR(64) | Displays the serial number as assigned from the certificate issuer. |
| FINGERPRINT | NVARCHAR(256) | Displays the hash of the entire certificate. It is used as a unique identifier in the certificate store. |
| CERTIFICATE | NCLOB | Displays the certificate as given during SQL. |

## Related Information

CREATE CERTIFICATE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-CERTIFICATE-Statement-System-Management.md) DROP CERTIFICATE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-CERTIFICATE-Statement-System-Management.md) PSE_CERTIFICATES System View [→](PSE_CERTIFICATES-System-View.md)
