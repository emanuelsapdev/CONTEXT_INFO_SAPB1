# 4.10.1.95 DROP LDAP PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 908–910

Drops an LDAP provider, and its associated credential, from the internal secure credential store.

## Syntax

```sql
DROP LDAP PROVIDER <ldap_provider_name>
```

## Syntax Elements

#### ldap_provider_name

The identifier for a valid LDAP provider previously created using the CREATE LDAP PROVIDER statement.

```sql
<ldap_provider_name> ::= <unicode_name>
```

## Description

Drops an LDAP provider.

If the dropped LDAP provider is the default LDAP provider, subsequent connections for users configured for LDAP authorization are impacted as follows:

- Any user connections created before the expiration of the value for the ldap_authorization_role_reuse_duration database property will succeed.
- Any user connections created after the expiration of the value for the ldap_authorization_role_reuse_duration database property will fail.
- Any first time user connections will fail.

With regards to LDAP authentication, if the default LDAP provider is dropped, subsequent user connections fail.

## Permissions

Only users with the LDAP ADMIN privilege can drop LDAP providers.

## Examples

The following example drops an LDAP provider called `my_ldap_provider`.

```sql
DROP LDAP PROVIDER my_ldap_provider;
```

## Related Information

CREATE LDAP PROVIDER Statement (Access Control) [→](CREATE-LDAP-PROVIDER-Statement-Access-Control.md) ALTER LDAP PROVIDER Statement (Access Control) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_PROVIDER_URLS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDER_URLS-System-View.md) LDAP_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDERS-System-View.md) LDAP_USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LDAP_USERS-System-View.md)
