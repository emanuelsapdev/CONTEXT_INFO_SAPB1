# 4.10.1.55 CREATE LDAP PROVIDER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 729–733

Creates an LDAP provider for use with LDAP authorization and authentication.

## Syntax

```sql
CREATE LDAP PROVIDER <ldap_provider_name>
 CREDENTIAL TYPE <credential_type_name> USING <credential_of_ldap_account>
 USER LOOKUP URL <url_string_literal>
 [ NESTED GROUP LOOKUP URL <url_string_literal> ]
 ATTRIBUTE DN <dn_string_literal>
 [ ATTRIBUTE MEMBER_OF <member_of_string_literal> ]
 [ SSL { ON | OFF } ]
 [ DEFAULT { ON | OFF } ]
 [ { ENABLE | DISABLE } PROVIDER ]
 [ ENABLE USER CREATION FOR LDAP [ <usertype_option> ] ]
```

## Syntax Elements

#### ldap_provider_name

Specifies the name of an LDAP provider you want to create.

```sql
<ldap_provider_name> ::= <unicode_name>
```

#### CREDENTIAL TYPE credential_type_name USING credential_of_ldap_account

Specifies the credential for the LDAP access account. Only one credential type can be configured for an LDAP provider and the only supported type is PASSWORD.

```sql
<credential_type_name> ::= 'PASSWORD'
<credential_of_ldap_account> ::=
'user=<user_dn_string_literal>;password=<passphrase>'
```

LDAP access account information includes the distinguished name (DN) and password of the user that is set up in LDAP server for use by SAP HANA server. This user must have permissions within the LDAP server to perform searches as specified by the USER LOOKUP URL and NESTED GROUP LOOKUP URL clauses.

For the credential type PASSWORD, specifies the credentials of an LDAP access account by using the USING clause.

`<credential_of_ldap_account>` specifies the credential of the LDAP access account that SAP HANA uses to log in to the LDAP server.

`<user_dn_string_literal>` specifies the distinguished name (DN) of the LDAP access account that HANA uses to log in to the LDAP server.

`<passphrase>` specifies the password for the access account that SAP HANA uses to log in to the LDAP server.

An example CREDENTIAL clause might look like this: `CREDENTIAL TYPE 'PASSWORD' USING 'user=cn=LookupAccount,o=largebank.com;password=secret'`.

#### USER LOOKUP URL url_string_literal

Specifies an LDAP URL that locates a unique user entry in the LDAP server that corresponds to an SAP HANA user. The format of a USER LOOKUP URL is as follows:

```sql
ldap[s]://<hostname>:<port>/<base_dn>?<attributes>?<scope>?<filter>
```

A search filter `<filter>` uses the USER_NAME of the SAP HANA user to locate the user entry in the LDAP Server.`<filter>` must include a condition of the form `'<attr>=*'` where `<attr>` is an LDAP attribute whose value is matched against the USER_NAME of the SAP HANA user. SAP HANA replaces the `'*'` in the search filter with the USER_NAME of the current SAP HANA user

For example, when the following LDAP query is sent to the LDAP server, `(&(objectClass=user) (sAMAccountName=*))` is replaced with `(&(objectClass=user)(sAMAccountName=<USER_NAME of the current or specified SAP HANA user>))`:

```sql
USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))'
```

`<filter>` must contain one and only one `'*'`; otherwise, an error is returned..

The `<attributes>` specification lists LDAP attributes whose values are returned to the SAP HANA server for a given user entry. `<attributes>` must be left empty for USER LOOKUP URL. SAP HANA constructs the `<attributes>` internally based on the LDAP attributes specified with ATTRIBUTE clause.

#### NESTED GROUP LOOKUP URL url_string_literal

Specifies an LDAP URL for obtaining LDAP group membership information, including nested groups, for a user from the LDAP server. For example: `NESTED GROUP LOOKUP URL 'ldap://myhostname:389/ ou=groupsOU,dc=x??sub?(member:1.2.840.113556.1.4.1941:=*)'`

The asterisk in `<url_string_literal>` is replaced by the user DN, which is obtained by using the USER LOOKUP URL.

Depending upon the NESTED GROUP LOOKUP URL, one or more levels of LDAP groups may be returned. It is possible to specify a URL that returns only one level of groups with NESTED GROUP LOOKUP URL. SAP HANA sends this LDAP query to the LDAP server for execution. Before sending the query, SAP HANA replaces '\*' in the NESTED GROUP LOOKUP URL with the DN of the user obtained from execution of USER LOOKUP URL.

While ATTRIBUTE MEMBER_OF and NESTED GROUP LOOKUP URL are both optional, if LDAP authorization is used and neither of these are defined, then an error is returned at run-time.

Support for nested LDAP groups is provided only when a single URL can be specified such that it returns a complete list of groups with the user’s membership (including groups with indirect membership). SAP HANA does not recursively fetch nested groups if they were not obtained by executing the search specified by NESTED GROUP LOOKUP URL.

#### ATTRIBUTE DN dn_string_literal

Specifies the LDAP attribute that provides the DN (distinguished name) of the LDAP User entry. The DN of the user is stored in the SAP HANA catalog.

#### ATTRIBUTE MEMBER_OF member_of_string_literal

Specifies the LDAP attribute that provides a list of groups that a user is a member of. If NESTED GROUP LOOOKUP URL is specified, then the group information is obtained using NESTED GROUP LOOKUP URL (that is, ATTRIBUTE MEMBER_OF is not used).

While ATTRIBUTE MEMBER_OF and NESTED GROUP LOOKUP URL are both optional, if LDAP authorization is used and neither of these are defined, then an error is returned at run-time.

#### SSL {ON | OFF}

Specifies whether SSL/TLS secures connections to the LDAP server, both for LDAP access account authentication and LDAP user and group searches. The default is OFF.

> **Caution**
>
> If using the LDAP server for user authorization and authentication, you must secure communication between SAP HANA and the LDAP server using the TLS/SSL protocol to protect the transmission of sensitive information such as user names, passwords, and group membership, which are otherwise sent in the clear between SAP HANA and the LDAP server.

When using SSL protocol, the trust store used to authenticate communication must be a certificate collection in the SAP HANA database with the purpose LDAP. The certificate of the Certificate Authority (CA) that signed the certificate used by the LDAP server must be available in this certificate collection. For more information, see the section on certificate management in the SAP HANA Security Guide.

When set to ON, the SSL/TLS protocol is used and the URL begins with "ldap://".

Connections to LDAP Server can also be secured by using Secure LDAP protocol. In this case, URL begins with “ldaps://”. SSL should be set to OFF when using Secure LDAP protocol.

#### DEFAULT {ON | OFF}

Designates the LDAP provider to use for LDAP authorization and authentication. The default is OFF.

You can create multiple named LDAP providers, but you can only designate one as the default. Designating an LDAP provider as DEFAULT removes the default designation of the previous default LDAP provider, if any.

#### {ENABLE | DISABLE } PROVIDER

Creates the provider as enabled or disabled. The default is DISABLE PROVIDER.

If a default LDAP provider is disabled, then users cannot log in by using LDAP authorization. VALIDATE LDAP PROVIDER can still be used to verify the configuration of a disabled LDAP provider.

#### ENABLE USER CREATION FOR

Enables automatic user creation when using LDAP authentication, and specifies type of the user to create - standard or restricted.

```sql
[ ENABLE USER CREATION FOR LDAP [ <usertype_option> ] ]
<usertype_option> ::= USER TYPE { STANDARD | RESTRICTED }
```

When enabling automatic user creation, optionally specify the type of the new users to be created. By default, new users are created as STANDARD users.

## Description

To use LDAP group-based authorization or LDAP authentication, access to an LDAP Server is configured in SAP HANA using an LDAP provider.

LDAP authentication and LDAP authorization require a default LDAP provider that is in an enabled state.

Nested LDAP groups is only supported when there is a single URL that can be used to return the complete list of groups that the user is a member of (including groups with indirect membership). Nested LDAP groups is not supported on directory servers that do not provide this capability.

## Permissions

Only users with the LDAP ADMIN privilege can create LDAP providers.

## Examples

**Example 1:** Create an LDAP provider, `my_ldap_provider`, for obtaining LDAP group memberships for SAP HANA users and activating it as the default LDAP provider for authorization.

```sql
CREATE LDAP PROVIDER my_ldap_provider
   CREDENTIAL TYPE 'PASSWORD' USING
'user=cn=LookupAccount,o=largebank.com;password=secret'
   USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))'
   ATTRIBUTE DN 'distinguishedName'
   ATTRIBUTE MEMBER_OF 'memberOf'
   SSL ON
   DEFAULT ON
   ENABLE PROVIDER;
```

**Example 2:** Create an LDAP provider to use nested groups:

```sql
CREATE LDAP PROVIDER my_ldap_provider
 CREDENTIAL TYPE 'PASSWORD' USING
'user=cn=LookupAccount,o=largebank.com;password=secret'
 USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))'
 NESTED GROUP LOOKUP URL 'ldap://myhostname:389/ou=groupsOU,dc=x??sub?(member:
1.2.840.113556.1.4.1941:=*)'
 ATTRIBUTE DN 'distinguishedName'
 SSL ON
 DEFAULT ON
 ENABLE PROVIDER;
```

**Example 3:** Create an LDAP provider configured for automatic creation of STANDARD users with LDAP authentication:

```sql
CREATE LDAP PROVIDER my_ldap_provider
 CREDENTIAL TYPE 'PASSWORD' USING
'user=cn=LookupAccount,o=largebank.com;password=secret'
 USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))'
ATTRIBUTE DN 'distinguishedName'
SSL ON
DEFAULT ON
ENABLE PROVIDER
ENABLE USER CREATION FOR LDAP;
```

**Example 4:** Configure an LDAP Provider for automatic creation of RESTRICTED users with LDAP authentication:

```sql
CREATE LDAP PROVIDER my_ldap_provider
  CREDENTIAL TYPE 'PASSWORD' USING
'user=cn=LookupAccount,o=largebank.com;password=secret'
  USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))'
  ATTRIBUTE DN 'distinguishedName'
  SSL ON
  DEFAULT ON
  ENABLE PROVIDER
  ENABLE USER CREATION FOR LDAP USER TYPE RESTRICTED;
```

## Related Information

ALTER LDAP PROVIDER Statement (Access Control) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-LDAP-PROVIDER-Statement-Access-Control.md) DROP LDAP PROVIDER Statement (Access Control) [→](DROP-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_PROVIDER_URLS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDER_URLS-System-View.md) LDAP_PROVIDERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDERS-System-View.md) LDAP_USERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LDAP_USERS-System-View.md)
