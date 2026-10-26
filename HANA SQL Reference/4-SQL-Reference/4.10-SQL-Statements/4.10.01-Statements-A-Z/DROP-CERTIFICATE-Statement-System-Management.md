# 4.10.1.83 DROP CERTIFICATE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 894–896

Drops a specified certificate from the list of certificates.

## Syntax

```sql
DROP CERTIFICATE <certificate_id>
```

## Syntax Elements

#### certificate_id

Specifies the certificate to be dropped.

```sql
<certificate_id> ::= <unsigned_integer>
```

## Description

The DROP CERTIFICATE statement drops this certificate from the list of certificates, which can be assigned to a PSE store. The statement succeeds only if the certificate is not assigned to a PSE store.

Information about certificates that are usable for assignment to PSE stores is stored in the CERTIFICATES system view.

## Permissions

Only users with the CERTIFICATE ADMIN system privilege are allowed to drop certificates.

## Examples

Create a certificate with subject and issuer SAP AG and a validity between 2011 and 2285. The certificate is shortened and the missing 21 lines mentioned as '...'.

```sql
CREATE CERTIFICATE FROM '-----BEGIN CERTIFICATE-----
MIIEVjCCAz6gAwIBAgIJAKZmSWxYxVmGMA0GCSqGSIb3DQEBBQUAMHkxCzAJBgNV
...
zn2Q+T5Og6ozD1WgUYsegJl3W2gNznEj66Ku1SDDzR0POjCnfK5xLt1WE5KBAIav
1SSbSTsw6rCRdg==
-----END CERTIFICATE-----' COMMENT 'Subject SAP AG Valid until 2285';
```

Check which certificate ID is used for the certificate created with the previous step.

```sql
SELECT CERTIFICATE_ID FROM CERTIFICATES WHERE COMMENT = 'Subject SAP AG Valid
until 2285';
```

Assuming the certificate ID was 12345678, you drop it.

```sql
DROP CERTIFICATE 12345678;
```

## Related Information

[CERTIFICATES System View](../../../6-System-Views-Reference/6.01-System-Views/CERTIFICATES-System-View.md)
