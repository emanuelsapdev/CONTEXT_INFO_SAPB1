# 4.10.1.44 CREATE CERTIFICATE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 699–700

Adds the specified certificate to the list of certificates.

## Syntax

```sql
CREATE CERTIFICATE FROM <certificate> [ COMMENT <comment> ]
```

## Syntax Elements

#### certificate

Specifies the certificate in PEM-representation, which should be stored in the database.

```sql
<certificate> ::= <string literal>
```

**comment** Adds a description for the certificate.

```sql
<comment> ::= <string_literal>
```

Use this value to help you find a specific certificate in the list of certificates.

## Description

The CREATE CERTIFICATE statement adds this certificate to the list of certificates, which can be assigned to a PSE store.

Information about certificates that are usable for assignment to PSE stores is stored in the CERTIFICATES system view.

## Permissions

Only users with the system privilege CERTIFICATE ADMIN can create certificates.

## Examples

Create a certificate with subject and issuer SAP AG and a validity between 2011 and 2285. The certificate is shortened and the missing 21 lines mentioned as '...'.

```sql
 CREATE CERTIFICATE FROM '-----BEGIN CERTIFICATE-----
MIIEVjCCAz6gAwIBAgIJAKZmSWxYxVmGMA0GCSqGSIb3DQEBBQUAMHkxCzAJBgNV
...
zn2Q+T5Og6ozD1WgUYsegJl3W2gNznEj66Ku1SDDzR0POjCnfK5xLt1WE5KBAIav
1SSbSTsw6rCRdg==
-----END CERTIFICATE-----' COMMENT 'Subject SAP AG Valid until 2285'
```

## Related Information

[CERTIFICATES System View](../../../6-System-Views-Reference/6.01-System-Views/CERTIFICATES-System-View.md)
