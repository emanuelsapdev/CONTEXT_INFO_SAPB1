# 4.10.1.115 DROP X509 PROVIDER (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 936–937

Drops an X.509 provider in the SAP HANA database.

## Syntax

```sql
DROP X509 PROVIDER <x509_provider_name> [ CASCADE ]
```

## Syntax Elements

#### x509_provider_name

Specifies which X.509 provider to drop.

```sql
<x509_provider_name> ::= <simple_identifier>
```

`<x509_provider_name>` must be an existing X.509 provider.

**CASCADE** Required only when the X.509 provider is referenced by a PSE's purpose object. The provider is removed from any PSE referencing it along with any user mappings for users authenticating with the provider. For PSEs where it is the only provider assigned, the purpose of that PSE is also removed.

## Permissions

Only database users with the USER ADMIN system privilege can drop an X.509 provider.

## Examples

Drops the X.509 provider, my_x509_provider1.

```sql
DROP X509 PROVIDER my_x509_provider1;
```

## Related Information

CREATE X509 PROVIDER (Access Control) [→](CREATE-X509-PROVIDER-Access-Control.md) ALTER X509 PROVIDER (Access Control) [→](ALTER-X509-PROVIDER-Access-Control.md) X509_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_PROVIDERS-System-View.md) X509_PROVIDER_RULES System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_PROVIDER_RULES-System-View.md) X509_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/X509_USER_MAPPINGS-System-View.md)
