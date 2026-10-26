# 4.10.1.53 CREATE JWT PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 725–727

Defines a JWT provider in the SAP HANA database.

## Syntax

```sql
CREATE JWT PROVIDER <jwt_provider_name> <issuer_clause>
   <external_id_clause> [ <case_clause> ]
```

## Syntax Elements

#### jwt_provider_name

Specifies the identifier of a JWT provider to be created. The JWT provider name must not already be defined.

```sql
<jwt_provider_name> ::= <simple_identifier>
```

#### issuer_clause

Sets JWT provider information.

```sql
<issuer_clause> ::= WITH ISSUER <issuer_claim>
<issuer_claim> ::= <string_literal>
```

`<issuer_claim>` is the issuer name provided in the iss claim of the JWT tokens issued by this JWT provider. `<issuer_claim>` must be unique across all JWT providers.

#### external_id_clause

Specifies the claim provided in the JWT tokens to use for mapping the HANA user to an external user name.

```sql
<external_id_clause> ::= CLAIM <string_literal> AS EXTERNAL IDENTITY
```

#### case_clause

Specifies whether the user mapping is checked case sensitive (default) or insensitive.

```sql
<case_clause> ::= CASE { SENSITIVE | INSENSITIVE } IDENTITY ]
```

## Permissions

Only database users that have the USER ADMIN system privilege can create a JWT provider.

## Examples

Create a JWT provider with the name my_jwt_provider, using issuer name www/url/my_url and claim user1. The identity checked by the provider is case sensitive.

```sql
CREATE JWT PROVIDER my_jwt_provider WITH ISSUER 'www/url/my_url'
   CLAIM 'user1' AS EXTERNAL IDENTITY CASE SENSITIVE IDENTITY;
```

## Related Information

[ALTER JWT PROVIDER Statement (Access Control)](ALTER-JWT-PROVIDER-Statement-Access-Control.md)

DROP JWT PROVIDER Statement (Access Control) [→](DROP-JWT-PROVIDER-Statement-Access-Control.md) JWT_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/JWT_PROVIDERS-System-View.md) JWT_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/JWT_USER_MAPPINGS-System-View.md)
