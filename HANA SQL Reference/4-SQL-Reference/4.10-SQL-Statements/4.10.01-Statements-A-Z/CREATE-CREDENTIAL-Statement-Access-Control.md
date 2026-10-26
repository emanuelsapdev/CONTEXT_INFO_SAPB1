# 4.10.1.47 CREATE CREDENTIAL Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 704–706

Creates a componentspecific or applicationspecific credential.

## Syntax

```sql
CREATE CREDENTIAL FOR [USER <user_name>] COMPONENT <component_id>
   PURPOSE <purpose_def> TYPE <type_def> [USING <using_param>]
```

## Syntax Elements

#### user_name

Specifies the user that can use the credential.

```sql
<user_name> ::= <unicode_name>
```

When this parameter is specified, the created credential is used for this database user only.

If USER `<user_name>` is not provided, then every user of the current instance uses the same credential when the following conditions are true:

- The user is using the specified component.
- The component needs access to the remote system specified by the PURPOSE parameter.

Only users with the CREDENTIAL ADMIN system privilege are allowed to alter credentials for other users.

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

Specifies a connection mechanism. For example 'PASSWORD' or 'KERBEROS'.

```sql
<type_def> ::= <string_literal>
```

#### using_param

Specifies the connection parameter.

```sql
<using_param> ::= <string_literal>
```

This value uses a type specified by the `<type_def>` parameter. It is required if the type is 'PASSWORD'.

## Description

The CREATE CREDENTIAL statement creates a componentspecific or applicationspecific credential.

## Permissions

This statement requires the CREDENTIAL ADMIN privilege.

## Examples

Create a credential for all users that is used by the component INTERNAL_APP. This credential uses the password mechanism for the PURPOSE COMPANY_MASTER_MACHINE.

```sql
CREATE CREDENTIAL FOR COMPONENT 'INTERNAL_APP' PURPOSE 'COMPANY_MASTER_MACHINE'
TYPE 'PASSWORD' USING 'PASSWORD_9876';
```

Create a credential for all users that is used by the component SAPHANAFEDERATION. This credential uses Kerberos for authentication.

```sql
CREATE CREDENTIAL FOR COMPONENT 'SAPHANAFEDERATION' PURPOSE 'H1' TYPE 'KERBEROS';
```

## Related Information

[CREDENTIALS System View](../../../6-System-Views-Reference/6.01-System-Views/CREDENTIALS-System-View.md)
