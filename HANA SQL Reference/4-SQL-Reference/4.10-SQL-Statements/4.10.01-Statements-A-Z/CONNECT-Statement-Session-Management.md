# 4.10.1.42 CONNECT Statement (Session Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 683–684

Connects to a database instance.

## Syntax

```sql
CONNECT {<user_name> PASSWORD <password>} | {WITH SAML ASSERTION <xml>}
```

## Syntax Elements

#### user_name

Specifies the user name for the connection.

```sql
<user_name> ::= <unicode_name>
```

#### WITH SAML ASSERTION xml

Specifies a SAML assertion to use when connecting to the database.

```sql
WITH SAML ASSERTION <xml>
 <xml> ::= <string_literal>
```

## Description

Connects to a database instance using either a user name and password pair or a SAML assertion for identification.

Automatic LDAP user creation is not supported with the CONNECT statement.

## Example

Create a SAML provider named ac_saml_provider specifying a subject and issuer for ACompany.

```sql
CREATE SAML PROVIDER ac_saml_provider
    WITH SUBJECT 'CN = wiki.detroit.ACompany.corp,OU = ACNet,O = ACompany,C = EN'
    ISSUER 'E = John.Do@acompany.com,CN = ACNetCA,OU = ACNet,O = ACompany,C =
EN';
```

Create a user called new_user with the password Password1. The user can connect to the system using the given password and with assertion of the SAML provider ac_saml_provider.

```sql
CREATE USER new_user PASSWORD Password1 WITH IDENTITY ANY FOR SAML PROVIDER
ac_saml_provider;
```

Connect to the database with the user name new_user and password Password1.

```sql
CONNECT new_user PASSWORD Password1;
```
