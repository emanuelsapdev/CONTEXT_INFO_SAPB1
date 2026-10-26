# 4.10.1.100 DROP SAML PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 914–916

Drops the specified SAML provider.

## Syntax

```sql
DROP SAML PROVIDER <saml_provider_name> CASCADE
```

## Syntax Elements

#### saml_provider_name

Specifies the name of the SAML provider to drop.

```sql
<saml_provider_name> ::= <simple_identifier>
```

`<saml_provider_name>` must be an existing SAML provider.

**CASCADE** Required only when the SAML purpose is referenced by a PSE's purpose object. The provider is removed from any PSE referencing it along with any user mappings for users authenticating with the provider. For PSEs where it is the only provider assigned, the purpose of that PSE is also removed.

## Description

If the SAML provider is currently used by an SAP HANA database user, then the SAML provider cannot be dropped when the CASCADE parameter is specified.

## Permissions

Only database users with the USER ADMIN system privilege can drop a SAML provider.

## Example

Drop the SAML provider named ac_saml_provider1.

```sql
DROP SAML PROVIDER ac_saml_provider1;
```

Drops the SAML provider, ac_saml_provider2, which is referenced by the PSE mypse1.

```sql
DROP SAML PROVIDER ac_saml_provider2 CASCADE;
```

## Related Information

PSE_PURPOSE_OBJECTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/PSE_PURPOSE_OBJECTS-System-View.md) SAML_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/SAML_PROVIDERS-System-View.md)
