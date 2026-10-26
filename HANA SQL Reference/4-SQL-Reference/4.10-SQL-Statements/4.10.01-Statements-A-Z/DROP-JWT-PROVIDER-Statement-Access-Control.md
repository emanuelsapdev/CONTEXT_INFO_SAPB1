# 4.10.1.93 DROP JWT PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 906–907

Drops a JWT provider in the SAP HANA database.

## Syntax

```sql
DROP JWT PROVIDER <jwt_provider_name> [ CASCADE ]
```

## Syntax Elements

#### jwt_provider_name

Specifies which JWT provider to drop.

```sql
<jwt_provider_name> ::= <simple_identifier>
```

`<jwt_provider_name>` must be an existing JWT provider.

**CASCADE** Required only when the JWT provider is referenced by a PSE's purpose object. The provider is removed from any PSE referencing it along with any user mappings for users authenticating with the provider. For PSEs where it is the only provider assigned, the purpose of that PSE is also removed.

## Description

If the JWT provider is in use by an SAP HANA database user, then the JWT provider cannot be dropped when the CASCADE parameter is specified.

## Permissions

Only database users that have the USER ADMIN system privilege can drop a JWT provider.

## Examples

Drops the JWT provider, my_jwt_provider1.

```sql
DROP JWT PROVIDER my_jwt_provider1;
```

Drops the JWT provider, my_jwt_provider2, which is referenced by the PSE mypse1.

```sql
DROP JWT PROVIDER my_jwt_provider2 CASCADE;
```

## Related Information

CREATE JWT PROVIDER Statement (Access Control) [→](CREATE-JWT-PROVIDER-Statement-Access-Control.md) ALTER JWT PROVIDER Statement (Access Control) [→](ALTER-JWT-PROVIDER-Statement-Access-Control.md) JWT_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/JWT_PROVIDERS-System-View.md) JWT_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/JWT_USER_MAPPINGS-System-View.md)
