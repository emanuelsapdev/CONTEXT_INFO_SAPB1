# 4.10.1.9 ALTER JWT PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 438–440

Alters a JWT provider in the SAP HANA database.

## Syntax

```sql
ALTER JWT PROVIDER <jwt_provider_name>
   { SET { [ <issuer_clause> ] [ <external_id_clause> ] }
   | <case_clause> }
```

## Syntax Elements

#### jwt_provider_name

Specifies the identifier of a JWT provider to be modified.

```sql
<jwt_provider_name> ::= <simple_identifier>
```

#### issuer_clause

Alters the issuer set for the provider.

```sql
<issuer_clause> ::= WITH ISSUER <issuer_claim>
<issuer_claim> ::= <string_literal>
```

`<issuer_claim>` must be unique across all JWT providers.

#### external_id_clause

Alters the claim set for the provider.

```sql
<external_id_clause> ::= CLAIM <string_literal> AS EXTERNAL IDENTITY
```

#### case_clause

Specifies whether the user mapping is checked case sensitive (default) or insensitive.

```sql
<case_clause> ::= CASE { SENSITIVE | INSENSITIVE } IDENTITY ]
```

## Description

For the SET clause, at least one of the two optional parameters must be specified.

## Permissions

Only database users that have the USER ADMIN system privilege can alter a JWT provider.

## Examples

Change the issuer of the y_jwt_provider JWT provider to www/url/my_new_url.

```sql
ALTER JWT PROVIDER my_jwt_provider SET ISSUER 'www/url/my_new_url';
```

Change the external identity of the y_jwt_provider JWT provider to user2.

```sql
ALTER JWT PROVIDER my_jwt_provider SET CLAIM 'user2' AS EXTERNAL IDENTITY;
```

Change the y_jwt_provider JWT provider to be case insensitive.

```sql
ALTER JWT PROVIDER my_jwt_provider CASE INSENSITIVE IDENTITY;
```

## Related Information

CREATE JWT PROVIDER Statement (Access Control) [→](CREATE-JWT-PROVIDER-Statement-Access-Control.md) DROP JWT PROVIDER Statement (Access Control) [→](DROP-JWT-PROVIDER-Statement-Access-Control.md) JWT_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/JWT_PROVIDERS-System-View.md) JWT_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/JWT_USER_MAPPINGS-System-View.md)
