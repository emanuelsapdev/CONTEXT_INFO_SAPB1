# 4.10.1.154 UNSET PSE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1111–1112

Removes the purpose for a PSE store.

## Syntax

```sql
UNSET PSE <pse_name> PURPOSE <purpose>
```

## Syntax Elements

#### pse_name

Specifies the name of the PSE store.

```sql
<pse_name> ::= <identifier>
```

#### purpose

Specifies the purpose of the PSE.

```sql
<purpose> ::=
 JWT
 | SAML
 | SAP LOGON
 | SSL
 | X509
 | LDAP
 | SOLACE
 | DATABASE REPLICATION
 | REMOTE SOURCE
```

## Description

Removes the assigned purpose for a PSE store along with any assigned purpose providers or hosts.

## Permissions

If you are not the owner of the PSE store, then you must have the REFERENCES privilege on the PSE object. For the SSL purpose, you must also have the SSL ADMIN system privilege. For the SAML or JWT purposes, you must also have the USER ADMIN system privilege. For all other authentication purposes, you must also have the TRUST ADMIN privilege.

## Examples

Remove the SSL purpose from the example_pse PSE store.

```sql
UNSET PSE example_pse PURPOSE SSL;
```

## Related Information

PSE_PURPOSE_OBJECTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/PSE_PURPOSE_OBJECTS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](CREATE-REMOTE-SOURCE-Statement-Access-Control.md) SET PSE Statement (System Management) [→](SET-PSE-Statement-System-Management.md) UNSET PSE Statement (System Management) [→](UNSET-PSE-Statement-System-Management.md)
