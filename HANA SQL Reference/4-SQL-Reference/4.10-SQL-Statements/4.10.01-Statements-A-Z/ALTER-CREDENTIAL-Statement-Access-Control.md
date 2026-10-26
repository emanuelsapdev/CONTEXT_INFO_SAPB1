# 4.10.1.4 ALTER CREDENTIAL Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 423–424

Modifies an existing componentspecific or applicationspecific credential.

## Syntax

```sql
ALTER CREDENTIAL FOR [USER <user_name>] COMPONENT <component_id>
   PURPOSE <purpose_def> TYPE <type_def> [USING <using_param>]
```

## Syntax Elements

#### user_name

Specifies the user that owns the credential.

```sql
<user_name> ::= <unicode_name>
```

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

Specifies a connection mechanism, such as 'PASSWORD' or 'KERBEROS'.

```sql
<type_def> ::= <string_literal>
```

#### using_param

Specifies the connection parameter. This is using a type specified by the `<type_def>` parameter. This value is required if the type is 'PASSWORD'.

```sql
<using_param> ::= <string_literal>
```

## Description

Only the credentials can be changed using this command. Each user can alter their own credentials.

## Permissions

This statement requires the CREDENTIAL ADMIN privilege.

## Example

Create a credential for all users that is used by the component INTERNAL_APP. This credential uses the password mechanism for the purpose COMPANY_MASTER_MACHINE.

```sql
CREATE CREDENTIAL FOR COMPONENT 'INTERNAL_APP' PURPOSE 'COMPANY_MASTER_MACHINE'
TYPE 'PASSWORD' USING 'PASSWORD_9876';
```

Change the password of the credential created in the previous step.

```sql
ALTER CREDENTIAL FOR COMPONENT 'INTERNAL_APP' PURPOSE 'COMPANY_MASTER_MACHINE'
TYPE 'PASSWORD' USING '1234_PASSWORD';
```

## Related Information

[CREDENTIALS System View](../../../6-System-Views-Reference/6.01-System-Views/CREDENTIALS-System-View.md)
