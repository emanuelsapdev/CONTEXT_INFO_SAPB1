# 4.10.1.21 ALTER USER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 623–633

Modifies the database user.

## Syntax

```sql
ALTER USER <user_name> {
   <remote_identity_option>
   | <password_validation_option> [ <validity_specification> ]
[ <user_parameter_option> ]
   | <usergroup_membership_option>
   | <validity_specification> [ <user_parameter_option> ]
   | <user_parameter_option>
   | <external_ident> [ <validity_specification> ] [ <user_parameter_option> ]
   | <reset_connect_attempts>
   | <drop_connect_attempts>
   | <password_lifetime>
   | <force_pass_change>
   | <user_activation_opts>
   | <authent_mech_opts>
   | <add_ident_opts>
   | <drop_ident_opts>
   | <add_remote_database_identity>
   | <drop_remote_database_identity>
 | <client_connect_option>
 | <special_privilege_handling>
 | <ldap_group_authorization>
}
```

## Syntax Elements

#### user_name

Specifies the username of the user to be modified.

```sql
<user_name> ::= <unicode_name>
```

#### remote_identity_option

Defines a remote database identification mechanism.

```sql
ADD REMOTE IDENTITY <remote_user_name> AT DATABASE <database_name>
```

##### remote_user_name

Specifies the remote user name.

```sql
<remote_user_name> ::= <unicode_name>
```

##### database_name

Specifies the remote database name.

```sql
<database_name> ::= <identifier>
```

#### password_validation_option

Specifies the user password.

```sql
<password_validation_option> ::= PASSWORD <password> [ NO
FORCE_FIRST_PASSWORD_CHANGE ]
```

The password must follow the rules defined for the current SAP HANA instance. The password rules include a minimal password length and a definition of which character types (lower, upper, digit, special characters) must be part of the password.

NO FORCE_FIRST_PASSWORD_CHANGE overrules the setting of the password policy parameter FORCE_FIRST_PASSWORD_CHANGE and allows the final password to be specified during user creation.

#### validity_specification

Specifies the validity specification with an optional user parameter option.

```sql
<validity_specification> ::= VALID <validity_opts>
```

##### validity_opts

Configures the user's temporal validity. The specified user is only allowed to connect within the given date range. Using this feature you can create users in advance or restrict the period when users can connect to the SAP HANA database.

```sql
<validity_opts> ::=
<from_specification> [ <until_specification> ]
| <until_specification>
```

##### from_specification

Sets when the user is valid from.

```sql
<from_specification> ::= FROM { <timestamp> | NOW }
```

Use the NOW keyword to configure the user account to be valid from the current time.

The default is NOW.

##### until_specification

Specifies when the user is valid until.

```sql
<until_specification> ::= UNTIL { <timestamp> | FOREVER }
```

Use the FOREVER keyword to configure the user account to never expire.

The default is FOREVER.

##### timestamp

Specifies a timestamp.

```sql
<timestamp> ::= <string_literal>
```

#### user_parameter_option

Sets or clears user parameters.

In the case of competing settings between user parameter options and workload class settings, a workload class setting takes precedence over a user parameter option. Workload class settings and user parameter options always take precedence over `.ini` file settings.

```sql
<user_parameter_option> ::=
 <set_user_parameters> [ <clear_user_parameter_option> ]
 | <clear_user_parameter_option>
```

##### set_user_parameters

Sets parameters in the user parameter list.

```sql
<set_user_parameters> ::= SET PARAMETER <user_parameter_list>
```

##### user_parameter_list

Specifies a list of user parameters.

```sql
<user_parameter_list> ::=
 <user_parameter> [, <user_parameter> [,…] ]
```

```sql
<user_parameter> ::= CLIENT = <string_literal>
 | LOCALE = <string_literal>
 | TIME ZONE  = <string_literal>
 | EMAIL ADDRESS = <string_literal>
 | RSERVE REMOTE SOURCES = '<remote_source_name>[,…]'
 | STATEMENT MEMORY LIMIT = '<integer>'
 | STATEMENT THREAD LIMIT = '<integer>'
```

| **User Parameter** | **Purpose** |
| --- | --- |
| CLIENT | When you define column store views, this parameter restricts the user's access to the specified client.<br>This parameter cannot be specified by users themselves. |
| LOCALE | When you define column store views, the user parameter LOCALE translates information according to the user's locale. |
| TIME ZONE | This parameter is not used by the SAP HANA database, but it can be read by external applications. |
| EMAIL ADDRESS | This parameter is not used by the SAP HANA database, but can be read by external applications. This value must be unique. |
| RSERVE REMOTE SOURCES | For use with the rserve adapter, this parameter specifies rserve remote sources. |
| STATEMENT MEMORY LIMIT | Sets a userspecific statement memory limit in gigabytes.<br>• If both a global and a user statement memory limit are set, then the user specific limit takes precedence, regardless of whether it is higher or lower than the global statement memory limit.<br>• If the userspecific statement memory limit is re moved, then the global limit takes effect for the user.<br>• Setting the statement memory limit to 0 disables any statement memory limit for the user.<br>• For STATEMENT MEMORY LIMIT to take effect, re source_tracking and memory_tracking must be active. |
| STATEMENT THREAD LIMIT | Sets a user specific concurrency limit on statements (despite the name, STATEMENT THREAD LIMIT is not an actual thread limit). Similar behaviors to STATE MENT MEMORY LIMIT apply for STATEMENT THREAD LIMIT. |
| PARAMETER PRIORITY | Sets a user-level priority value for all statements in the current connection; the range of possible values is from 0 to 9 (the default is 5). |

##### clear_user_parameter_option

Clears one or more user parameters.

```sql
<clear_user_parameter_option> ::=
 CLEAR PARAMETER <clear_user_parameter_list>
 | CLEAR ALL PARAMETERS
<clear_user_parameter_list> ::=
 <clear_user_parameter> [, <clear_user_parameter> [,…] ]
```

For the list of parameters you can clear, refer to the list you can set in the `<user_parameter_list>` in the previous clause.

#### usergroup_membership_option

Adds or removes a user from a user group. A user can only be a member of one user group at a time.

```sql
<usergroup_membership_option> ::=
 SET USERGROUP <usergroup_name>
 | UNSET USERGROUP
```

##### SET USERGROUP usergroup_name

Adds the user to the specified user group.

##### UNSET USERGROUP

Removes the user from the specified user group.

When adding and removing a user to/from a user group, you must have the appropriate privileges for the user group you are adding to and removing from, as follows:

- For user groups defined as ENABLE USER ADMIN, you must have USER ADMIN privilege, or USERGROUP OPERATOR privilege on the user group, to add/remove users.
- For user groups defined as DISABLE USER ADMIN, you must have USERGROUP OPERATOR privilege on the user group to add/remove users.

#### external_ident

Specifies the external identity for the user. This clause is only for Kerberos authentication.

```sql
IDENTIFIED EXTERNALLY AS <external_identity> [ VALID
<validity_specification> ]
```

##### external_identity

Defines an external identity that authenticates the user.

```sql
<external_identity> ::=
 <simple_identifier>
 | <string_literal>
```

#### reset_connect_attempts

Resets the number of invalid connection attempts to zero so the user can connect immediately.

```sql
<reset_connect_attempts> ::= RESET CONNECT ATTEMPTS
```

You need the USER ADMIN privilege to use this command.

For the maximum number of allowed invalid connection attempts before a user is locked, see the M_PASSWORD_POLICY system view.

#### drop_connect_attempts

Drops old information about invalid connect attempts recorded for the specified user.

```sql
<drop_connect_attempts> ::= DROP CONNECT ATTEMPTS
```

It does not reset the current count of invalid connect attempts and therefore does not allow the user to connect immediately.

This option can be used by the user themselves or by a user with the USER ADMIN privilege.

To view the count of invalid connection attempts that have occurred, see the INVALID_CONNECT_ATTEMPTS system view.

#### password_lifetime

Enables or disables password lifetime checks.

```sql
<password_lifetime> ::= { ENABLE | DISABLE } PASSWORD LIFETIME
```

You need the USER ADMIN privilege to use this command.

#### force_pass_change

Forces the user to change their password immediately after the next connection to the SAP HANA database.

```sql
<force_pass_change> ::= FORCE PASSWORD CHANGE
```

You need the USER ADMIN privilege to use this command.

#### user_activation_opts

Activates or deactivates a user's account.

```sql
<user_activation_opts> ::= { ACTIVATE | DEACTIVATE } [ USER NOW ]
```

Users cannot connect to the SAP HANA database once their account is deactivated. However, it may appear as though deactivated users are still active in the system (for example when a procedure that was created by the user with DEFINER MODE is called). Reactivate a deactivated user with the ACTIVATE keyword. Activating and reactivating a user requires the USER ADMIN privilege.

#### authent_mech_opts

Enables or disables the selected authentication mechanism.

```sql
<authent_mech_opts> ::= { ENABLE | DISABLE } <authentication_mechanism>
```

##### authentication_mechanism

Specifies the type of the authentication mechanism to enable or disable.

```sql
<authentication_mechanism> ::=
 PASSWORD
 | KERBEROS
 | SAML
 | X509
 | SAP LOGON TICKET
 | SAP ASSERTION TICKET
 | JWT
 | LDAP
```

#### add_ident_opts

Defines a method for authenticating the user.

```sql
<add_ident_opts> ::=
 ADD IDENTITY { <add_provider_identity> [ <add_provider_identity> […] ]
 | { <external_identity> FOR KERBEROS } }
<add_provider_identity> ::=
 <saml_provider_ident>
 | <x509_provider_ident>
 | <kerberos_provider_ident>
 | <logon_ticket_ident>
 | <assertion_ticket_ident>
 | <jwt_provider_ident>
```

##### saml_provider_ident

Defines a SAML provider.

```sql
<saml_provider_ident> = <mapped_user_name> FOR SAML PROVIDER
<saml_provider_name>
<mapped_user_name> ::= ANY | <string_literal>
<saml_provider_name> ::= <simple_identifier>
```

`<mapped_user_name>` specifies the mapped SAML user name to use. If the keyword ANY is used, then the SAML assertion contains the name of the database user that the assertion is valid for.

`<saml_provider_name>` specifies the identifier of a SAML provider that already exists in the system.

For more information on SAML providers, see the CREATE SAML PROVIDER statement.

##### x509_provider_ident

Defines an X.509 certificate issuer or X.509 provider.

```sql
<x509_provider_ident> ::=
   <subject_distinguished_name> ISSUER <issuer_distinguished_name> FOR X509
   | { '<subject_distinguished_name>' | ANY } FOR X509 PROVIDER
<x509_provider_name>
<subject_distinguished_name> ::= <string_literal>
<issuer_distinguished_name> ::= <string_literal>
<x509_provider_name> ::= <simple_identifier>
```

`<subject_distinguished_name>` specifies the subject name provided in the certificate of the X. 509 identity provider.

`<issuer_distinguished_name>` specifies the issuer name provided in the certificate of the X.509 identity provider.

You can specify a wildcard (ANY) for the subject name only for an X.509 provider with matching rules.

`<x509_provider_name>` specifies the identifier of an X.509 provider that already exists in the system.

##### kerberos_provider_ident

Defines a KERBEROS identity.

```sql
<kerberos_provider_ident> ::= <kerberos_principal_name> FOR KERBEROS
<kerberos_principal_name> ::= <string_literal>
```

`<kerberos_principal_name>` specifies an identity within an external authentication system.

##### logon_ticket_ident

Sets SAP Logon Ticket as the authentication method.

```sql
<logon_ticket_ident> ::= FOR SAP LOGON TICKET
```

##### assertion_ticket_ident

Sets SAP Assertion Ticket as the authentication method.

```sql
<assertion_ticket_ident> ::= FOR SAP ASSERTION TICKET
```

##### jwt_provider_ident

Defines a JWT provider-user-mapping.

```sql
<jwt_provider_ident> ::= <mapped_user_name> FOR JWT PROVIDER
<jwt_provider_name>
<mapped_user_name> ::= { ANY | <string_literal> }
<jwt_provider_name> ::= <simple_identifier>
```

`<mapped_user_name>` specifies the mapped JWT user name to use. If the keyword ANY is used, then the JWT token contains the name of the database user that the token is valid for.

`<jwt_provider_name>` specifies the identifier of a JWT provider already existing in the system.

#### drop_ident_opts

Drops the defined identity provider.

```sql
<drop_ident_opts> =
 DROP IDENTITY { <provider_info> [ <provider_info> […] ] | FOR KERBEROS }
```

##### provider_info

Specifies the provider info to be dropped.

```sql
<provider_info> ::=
 FOR SAML PROVIDER <saml_provider_name>
 | <subject_distinguished_name> ISSUER <issuer_distinguished_name> FOR X509
 | [ '<subject_distinguished_name>' | ANY ] FOR X509 PROVIDER
<x509_provider_name>
 | FOR JWT PROVIDER <jwt_provider_name>
 | FOR SAP LOGON TICKET
 | FOR SAP ASSERTION TICKET
```

#### add_remote_database_identity

Adds a remote database identity.

```sql
ADD REMOTE IDENTITY <remote_user_name> AT DATABASE <database_name>
```

#### drop_remote_database_identity

Drops a remote database identity.

```sql
DROP REMOTE IDENTITY <remote_user_name> AT DATABASE <database_name>
```

#### client_connect_option

Enables or disables the client from connecting at all. In case of disabled client connect, only connecting via an XS application is allowed.

```sql
<client_connect_option> ::= { ENABLE | DISABLE } CLIENT CONNECT
```

#### special_privilege_handling

Allows a user with the USER ADMIN privilege to control whether another user can create objects in their own schema, and whether the user has the PUBLIC role.

When a user is created, they are automatically granted PUBLIC and CREATE ANY for objects in their schema, and these are granted by user SYS. `<special_privilege_handling>` allows users with the USER ADMIN privilege to remove (or re-grant) CREATE ANY and PUBLIC. Users that do not have the PUBLIC role and do not have the CREATE ANY ON OWN SCHEMA privilege are indicated in the USERS system view as restricted users.

```sql
<special_privilege_handling> ::=
 { GRANT | REVOKE } CREATE ANY ON OWN SCHEMA
 | { GRANT | REVOKE } ROLE PUBLIC
```

Use the GRANT | REVOKE CREATE ANY ON OWN SCHEMA clause to grant or revoke, respectively, a user's ability to create objects in their own schema.

Use the GRANT | REVOKE ROLE PUBLIC clause to grant or revoke, respectively, PUBLIC role from a user.

#### ldap_group_authorization

Specifies the LDAP group authorization mode for the user.

```sql
<ldap_group_authorization> ::= AUTHORIZATION { LOCAL | LDAP }
```

##### LOCAL

Specifies the use of local authorization mode for the user. This is the default.

##### LDAP

Specifies the use of LDAP authorization mode for the user.

Users with LDAP authorization mode cannot be granted permissions directly and cannot have local roles granted to them.

When changing the LDAP authorization mode from LOCAL authorization to LDAP for a user, LDAP roles are evaluated and activated upon next login. Also, local roles and privileges granted to the user are revoked except for roles that are granted by SYS--for example, the PUBLIC role--and the CREATE ANY privilege on the user's own schema.

## Description

Users configured for LDAP authentication cannot simultaneously be configured for local password authentication. Local password authentication must be disabled before a user can be configured for LDAP authentication, for example, using ALTER USER...DISABLE PASSWORD.

External users are authenticated by using an external system, for example a Kerberos system. For detailed information about external identities, contact your domain administrator.

## Permissions

Every database user has the required privileges to call the ALTER USER statement. However, some of the options for this command required additional database privileges.

Administrators can use the ALTER USER statement to configure other user accounts as long as they have the USER ADMIN privilege.

## Configuration Parameters

Configuration parameters concerning the user's password can be observed with the M_PASSWORD_POLICY system view. These parameters are stored in `indexserver.ini`, in the password policy section.

The description of the parameters concerned can be found in the Appendix of the SAP HANA Security Guide under Password Policy Parameters.

## Examples

Create a SAML provider named ac_saml_provider in the database specifying a subject and issuer for ACompany.

```sql
CREATE SAML PROVIDER ac_saml_provider
   WITH SUBJECT 'CN = wiki.detroit.ACompany.corp,OU = ACNet,O = ACompany,C = EN'
   ISSUER 'E = John.Do@acompany.com,CN = ACNetCA,OU = ACNet,O = ACompany,C = EN';
```

Create a new user named new_user that can connect by using a password or with an assertion of the SAML provider ac_saml_provider. The `<mapped_user_name>` was set to ANY as the assertion provides the database user name.

```sql
CREATE USER new_user PASSWORD Password1 WITH IDENTITY ANY FOR SAML PROVIDER
ac_saml_provider;
```

Force the user to change their password.

```sql
ALTER USER new_user FORCE PASSWORD CHANGE;
```

Disable SAML authentication for the user.

```sql
ALTER USER new_user DISABLE SAML;
```

Reset the number of invalid connection attempts to zero for new_user.

```sql
ALTER USER new_user RESET CONNECT ATTEMPTS;
```

Define the external identity for KERBEROS and enable KERBEROS for this user. Adding an external identification mechanism to a user does not automatically enable it. You must do this as a separate step as shown in this example.

```sql
ALTER USER new_user ADD IDENTITY 'testkerberosName' FOR KERBEROS;
ALTER USER new_user ENABLE KERBEROS;
```

Remove the ac_saml_provider SAML provider identity from new_user.

```sql
ALTER USER new_user DROP IDENTITY FOR SAML PROVIDER ac_saml_provider;
```

Disable the account.

```sql
ALTER USER new_user DEACTIVATE;
```

## Related Information

CREATE USER Statement (Access Control) [→](CREATE-USER-Statement-Access-Control.md) USERGROUPS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERGROUPS-System-View.md) USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) SQL Notation Conventions [→](../../4.02-SQL-Notation-Conventions.md) Data Types [→](../../4.03-Data-Types/README.md) M_PASSWORD_POLICY System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_PASSWORD_POLICY-System-View.md) INVALID_CONNECT_ATTEMPTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/INVALID_CONNECT_ATTEMPTS-System-View.md) CREATE SAML PROVIDER Statement (Access Control) [→](CREATE-SAML-PROVIDER-Statement-Access-Control.md) USER_PARAMETERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/USER_PARAMETERS-System-View.md) SAML_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/SAML_PROVIDERS-System-View.md) SAML_USER_MAPPINGS System View [→](../../../6-System-Views-Reference/6.01-System-Views/SAML_USER_MAPPINGS-System-View.md)
