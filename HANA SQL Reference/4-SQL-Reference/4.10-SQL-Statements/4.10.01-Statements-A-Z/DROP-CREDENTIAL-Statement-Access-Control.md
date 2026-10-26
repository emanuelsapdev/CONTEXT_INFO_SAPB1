# 4.10.1.87 DROP CREDENTIAL Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 900–901

Drops an existing componentspecific or applicationspecific credential.

## Syntax

```sql
DROP CREDENTIAL FOR [USER <user_name>] COMPONENT <component_id>
   PURPOSE <purpose_def> TYPE <type_def>
```

## Syntax Elements

#### user_name

Specifies the owner of the credential to be dropped.

```sql
<user_name> ::= <unicode_name>
```

Only users with the CREDENTIAL ADMIN system privilege can drop credentials for other users.

#### component_id

Specifies an identifier for the component that uses the credential.

```sql
<component_id> ::= <string_literal>
```

#### purpose_def

Specifies the applicationspecific or componentspecific purpose string.

```sql
<purpose_def> ::= <string_literal>
```

#### type_def

Specifies a connection mechanism; for example 'PASSWORD'.

```sql
<type_def> ::= <string_literal>
```

## Description

Each user can drop credentials that they own.

## Permissions

This statement requires the CREDENTIAL ADMIN privilege.

## Example

Create a credential for user WORKER that is used by the component INTERNAL_APP. This credential uses the password mechanism for the PURPOSE COMPANY_MASTER_MACHINE.

```sql
CREATE CREDENTIAL FOR USER WORKER COMPONENT 'INTERNAL_APP' PURPOSE
'COMPANY_MASTER_MACHINE' TYPE 'PASSWORD' USING 'PASSWORD_9876';
```

Drop the credential.

```sql
DROP CREDENTIAL FOR USER WORKER COMPONENT 'INTERNAL_APP' PURPOSE
'COMPANY_MASTER_MACHINE' TYPE 'PASSWORD';
```

## Related Information

[CREDENTIALS System View](../../../6-System-Views-Reference/6.01-System-Views/CREDENTIALS-System-View.md)
