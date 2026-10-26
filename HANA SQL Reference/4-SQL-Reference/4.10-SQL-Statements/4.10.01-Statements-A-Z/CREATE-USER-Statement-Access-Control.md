# 4.10.1.71 CREATE USER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 844–853

Creates a new database user.

## Syntax

```sql
CREATE [ RESTRICTED ] USER <user_name>
 [ <authentication_options> ]
 [ <validity_specification> ]
 [ <set_user_parameters> ]
 [ <ldap_group_authorization> ]
 [ <usergroup_membership_option> ]
```

## Syntax Elements

#### user_name

Specifies the user name of the user to be created.

```sql
<user_name> ::= <unicode_name>
```

**authentication_options** Specifies the authentication options for the user.

```sql
<authentication_options> ::=
 { <remote_identity_option>
  | <password_option>
  | <external_ident>
 | <with_ident_opts>
}
```

##### remote_identity_option

Specifies a database user in another tenant database as the remote identity of the database user being created.

```sql
<remote_identity_option> ::=
 <remote_database_identity> [ <remote_database_identity> […] ]
<remote_database_identity> ::= <remote_user_name> AT DATABASE
<database_name>
<remote_user_name> ::= <simple_identifier>
<database_name> ::= <identifier>
```

##### password_option

Specifies the user password of the user being created.

```sql
<password_option> ::= PASSWORD <password> [ NO
FORCE_FIRST_PASSWORD_CHANGE ]
```

The option NO FORCE_FIRST_PASSWORD_CHANGE overrules the setting of the password policy parameter force_first_password_change and allows the final password to be specified during user creation.

The password must follow the rules defined for the current SAP HANA instance. The password rules include a minimum password length and a definition of which character types (lower, upper, digit, special characters) must be part of the password.

##### external_ident

Specifies the external identity for the user. This clause is only for Kerberos authentication.

```sql
<external_ident> ::= IDENTIFIED EXTERNALLY AS <external_identity>
```

###### external_identity

Defines an external identity for user authentication.

```sql
<external_identity> ::=
 <simple_identifier>
 | <string_literal>
```

##### with_ident_opts

Defines a method for user authentication.

```sql
<with_ident_opts> ::= WITH IDENTITY <provider_identity>
[ <provider_identity> […] ]
<provider_identity> ::=
<saml_provider_ident>
 | <x509_provider_ident>
 | <kerberos_provider_ident>
 | <logon_ticket_ident>
 | <assertion_ticket_ident>
 | <jwt_provider_ident>
 | <ldap_provider_ident>
```

###### saml_provider_ident

Defines a SAML provider.

```sql
<saml_provider_ident> ::= <mapped_user_name> FOR SAML PROVIDER
<saml_provider_name>
<mapped_user_name> ::= { ANY | <string_literal> }
<saml_provider_name> ::= <simple_identifier>
```

`<mapped_user_name>` specifies the mapped SAML user name to use. If the keyword ANY is used, then the SPProvidedID attribute of the SAML assertion contains the name of the database user that the assertion is valid for. For more information, see the section on single sign-on using SAML in the SAP HANA Security Guide.

`<saml_provider_name>` specifies the identifier of a SAML provider that already exists in the system.

###### x509_provider_ident

Defines an X.509 certificate issuer or X.509 provider.

```sql
<x509_provider_ident> ::=
   <subject_distinguished_name> ISSUER <issuer_distinguished_name> FOR
X509
   | { '<subject_distinguished_name>' | ANY } FOR X509 PROVIDER
<x509_provider_name>
<subject_distinguished_name> ::= <string_literal>
<issuer_distinguished_name> ::= <string_literal>
<x509_provider_name> ::= <simple_identifier>
```

`<subject_distinguished_name>` specifies the subject name provided in the certificate of the X.509 identity provider.

`<issuer_distinguished_name>` specifies the issuer name provided in the certificate of the X. 509 identity provider.

You can specify a wildcard (ANY) for the subject name only for an X.509 provider with matching rules.

`<x509_provider_name>` specifies the identifier of an X.509 provider that already exists in the system.

###### kerberos_provider_ident

Defines a KERBEROS identity.

```sql
<kerberos_provider_ident> ::= <kerberos_principal_name> FOR KERBEROS
<kerberos_principal_name> ::= <string_literal>
```

`<kerberos_principal_name>` specifies an identity within an external authentication system.

###### logon_ticket_ident

Sets SAP Logon Ticket as the authentication method.

```sql
<logon_ticket_ident> ::= FOR SAP LOGON TICKET
```

###### assertion_ticket_ident

Sets SAP Assertion Ticket as the authentication method.

```sql
<assertion_ticket_ident> ::= FOR SAP ASSERTION TICKET
```

###### jwt_provider_ident

Defines a JWT provider-user-mapping.

```sql
<jwt_provider_ident> ::= <mapped_user_name> FOR JWT PROVIDER
<jwt_provider_name>
<mapped_user_name> ::= { ANY |
<string_literal> }
<jwt_provider_name> ::= <simple_identifier>
```

`<mapped_user_name>` specifies the mapped JWT user name to use. If the keyword ANY is used, then the JWT token will contain the name of the database user that the token is valid for.

`<jwt_provider_name>` specifies the identifier of a JWT provider that already exists in the system.

###### ldap_provider_ident

Creates a user enabled to use LDAP authentication.

```sql
<ldap_provider_ident> ::= FOR LDAP PROVIDER
```

#### validity_specification

Defines the validity specification with an optional user parameter option.

```sql
<validity_specification> ::= VALID <validity_opts>
```

##### validity_opts

Configures the user's temporal validity.

```sql
<validity_opts> ::=
 <from_specification> [ <until_specification> ]
 | <until_specification>
```

The specified user can only connect within the given date range. By using this feature, you can create users in advance or restrict the period when users can connect to the SAP HANA database.

##### from_specification

Sets when the user is valid from.

```sql
<from_specification> ::= FROM { <timestamp> | NOW }
```

Use the NOW keyword to configure the user account to be valid from the current time.

The default value is NOW.

##### until_specification

Sets when the user is valid until.

```sql
<until_specification> ::= UNTIL { <timestamp> | FOREVER }
```

Use the FOREVER keyword to configure the user account to never expire.

The default value is FOREVER.

##### timestamp

Specifies a timestamp.

```sql
<timestamp> ::= <string_literal>
```

#### set_user_parameters

Sets parameters in the user parameter list.

```sql
<set_user_parameters> ::= SET PARAMETER <user_parameter_list>
```

##### user_parameter_list

Specifies a list of user parameters.

```sql
<user_parameter_list> ::=
 <user_parameter>  [, <user_parameter> [,…] ]
```

##### user_parameter

Defines user parameters.

```sql
<user_parameter> ::=
 CLIENT = <string_literal>
 | LOCALE = <string_literal>
 | TIME ZONE  = <string_literal>
 | EMAIL ADDRESS = <string_literal>
 | STATEMENT MEMORY LIMIT = '<integer>'
 | STATEMENT THREAD LIMIT = '<integer>'
  | STATEMENT THREAD LIMIT = '<integer>'
```

| **User Parameter** | **Purpose** |
| --- | --- |
| CLIENT | When you define column store views, the user parameter CLIENT restricts the access of the user to the speci fied client.<br>This parameter is for internal use only. |
| LOCALE | When you define column store views, the user parameter LOCALE translates information according to the user's locale. |
| TIME ZONE | Not used by the SAP HANA database, but can be read by external applications. |
| EMAIL ADDRESS | Not currently used by the SAP HANA database, but can be read by external applications. This value must be unique. |
| STATEMENT MEMORY LIMIT | Sets a user specific statement memory limit in gigabytes.<br>• If both a global and a user statement memory limit are set, then the userspecific limit takes precedence, regardless of whether it is higher or lower than the global statement memory limit.<br>• If the userspecific statement memory limit is re moved, then the global limit takes effect for the user.<br>• Setting the statement memory limit to 0 disables any statement memory limit for the user.<br>• For STATEMENT MEMORY LIMIT to take effect, re source_tracking and memory_tracking must be active. |
| STATEMENT THREAD LIMIT | Sets a userspecific concurrency limit on statements (despite the name, STATEMENT THREAD LIMIT is not an actual thread limit). Similar behaviors to STATE MENT MEMORY LIMIT apply to STATEMENT THREAD LIMIT. |
| PARAMETER PRIORITY | Sets a user-level priority value for all statements in the current connection; the range of possible values is from 0 to 9 (the default is 5). |

#### ldap_group_authorization

Specifies the LDAP group authorization mode for the user.

```sql
<ldap_group_authorization> ::= AUTHORIZATION { LOCAL | LDAP }
```

##### LOCAL

Specifies the use of local authorization mode for the user. This is the default.

When changing the LDAP authorization mode from LDAP to LOCAL for a user, roles that were granted using LDAP are revoked, and the DN value for the SAP HANA user is cleared.

##### LDAP

Specifies the use of LDAP authorization mode for the user.

Users with LDAP authorization mode cannot be granted permissions directly, and cannot have local roles granted to them.

When changing the LDAP authorization mode from LOCAL authorization to LDAP for a user, LDAP roles are evaluated and activated upon next login. Also, local roles and privileges granted to the user are revoked except for roles that are granted by SYS--for example, the PUBLIC role--and the CREATE ANY privilege on the user's own schema.

#### usergroup_membership_option

Adds the user to the specified user group.

```sql
SET USERGROUP <usergroup_name>
```

You must have the USER ADMIN privilege to add a user to a user group, unless the user group is defined as DISABLE USERGROUP OPERATOR, in which case you must have the USERGROUP OPERATOR privilege on `<usergroup_name>`.

When adding a user to a user group, you must have the appropriate privileges for the user group you are adding to, as follows:

- For user groups defined as DISABLE USER ADMIN, you must have USERGROUP OPERATOR privilege on the user group to add users.
- For user groups that are not defined as DISABLE USER ADMIN, you must have USER ADMIN privilege, or USERGROUP OPERATOR privilege on the user group, to add users.

## Description

The specified user name must not be identical to the name of an existing user, usergroup, role, or schema.

There are some users that are delivered with the SAP HANA database: SYS, SYSTEM, and a number of users with the _SYS_ prefix.

Users in the database can be authenticated by varying mechanisms:

- Internal authentication mechanism using a password.
- External mechanisms such as Kerberos, SAML, SAP Logon Ticket, SAP Assertion Ticket, or X.509.

A user can be authenticated by more than one mechanism at a time; however, only one password and one principal name for Kerberos can be valid at any one time.

Specify at least one authentication mechanism to allow the user to connect and work with the database instance. For backwards compatibility, the IDENTIFIED EXTERNALLY AS `<external_identity>` syntax is maintained. This syntax essentially performs the same function as the `<kerberos_principal_name>` FOR KERBEROS syntax.

External users are authenticated by using an external system, for example a Kerberos system. For detailed information about external identities, contact your domain administrator.

A schema with the user's name is created for each database user: this schema cannot be explicitly dropped. The user's schema is automatically dropped when the user is deleted. The database user owns this schema and it is used as their default schema when they execute a command without explicitly specifying a schema name.

Users created without the RESTRICTED option can create any object in their own schema and they are granted the role PUBLIC allowing them to select any system view. Users created with the RESTRICTED option have no privileges, not even the ability to create objects in their own schema. These users are meant for using specific applications only. All privileges needed for the application have to be granted to such users, preferably using a role combined with the application.

## Permissions

Only database users with the USER ADMIN privilege, or USERGROUP OPERATOR privilege on a user group, are allowed to create a database user.

## Configuration Parameters

Configuration parameters concerning the user's password can be observed with the monitoring view M_PASSWORD_POLICY. These parameters are stored in the password policy section of the `indexserver.ini` file.

The description of the parameters concerned can be found in the Appendix of the SAP HANA Security Guide under Password Policy Parameters.

## Examples

## Example 1 - Create user with password

The following example shows you how to create a user `T12345` with a password `Password123`.

```sql
CREATE USER T12345 PASSWORD Password123;
```

## Example 2 - Create user that uses an external authentication mechanism

The following example creates an SAML provider named `ac_saml_provider` in the database, specifying a subject and issuer for `ACompany`.

```sql
CREATE SAML PROVIDER ac_saml_provider
    WITH SUBJECT 'CN = wiki.detroit.ACompany.corp,OU = ACNet,O = ACompany,C = EN'
    ISSUER 'E = John.Do@acompany.com,CN = ACNetCA,OU = ACNet,O = ACompany,C =
EN';
```

The following example creates a new user called `new_user` with password `Password1`. The user can connect to the system by using the given password and with an assertion of the existing SAML provider `ac_saml_provider`. The `<mapped_user_name>` is set to `ANY` as the assertion provides the database user name.

```sql
CREATE USER new_user PASSWORD Password1 WITH IDENTITY ANY FOR SAML PROVIDER
ac_saml_provider;
```

The following example creates a user that is only allowed to log in using X509:

```sql
CREATE USER testuser WITH IDENTITY 'C=US, ST=VA, L=Fairfax, O=example.com,
CN=testuser' ISSUER 'C=US, ST=VA, L=Fairfax, O=example.com, CN=Root CA' FOR X509;
```

The following example creates a user that is only allowed to log in using password or X509:

```sql
CREATE USER testuser PASSWORD BadPassword5 WITH IDENTITY 'C=US, ST=VA,
L=Fairfax, O=example.com, CN=testuser' ISSUER 'C=US, ST=VA, L=Fairfax,
O=example.com, CN=Root CA' FOR X509;
```

The following example creates a user that is only allowed to log in using X509 and whose account is deactivated on Jan 1, 2028:

```sql
CREATE USER testuser WITH IDENTITY 'C=US, ST=VA, L=Fairfax, O=example.com,
CN=testuser' ISSUER 'C=US, ST=VA, L=Fairfax, O=example.com, CN=Root CA' FOR X509
VALID UNTIL '2028-01-01';
```

The following example creates a user that is only allowed to log in using SAML (this statement actually throws an error if the SAML provider does not exist):

```sql
CREATE USER testuser WITH IDENTITY ANY FOR SAML PROVIDER nonexistandsamlprovider;
```

## Example 3 - Create user that is associated with a remote user

This example creates a new user called `USER1` associated with the user `USER2` at the remote database `DB2`.

```sql
CREATE USER USER1 WITH REMOTE IDENTITY USER2 AT DATABASE DB2;
```

## Related Information

CREATE SAML PROVIDER Statement (Access Control) [→](CREATE-SAML-PROVIDER-Statement-Access-Control.md) CREATE JWT PROVIDER Statement (Access Control) [→](CREATE-JWT-PROVIDER-Statement-Access-Control.md) M_PASSWORD_POLICY System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PASSWORD_POLICY-System-View.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) USER_PARAMETERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USER_PARAMETERS-System-View.md) INVALID_CONNECT_ATTEMPTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/INVALID_CONNECT_ATTEMPTS-System-View.md) SAML_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/SAML_PROVIDERS-System-View.md) SAML_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/SAML_USER_MAPPINGS-System-View.md)
