# 4.10.1.19.14 ALTER LDAP PROVIDER Statement (Access Control)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 489–494

Updates an LDAP provider for use with LDAP authorization and authentication.

## Syntax

```sql
ALTER LDAP PROVIDER <ldap_provider_name>
 [ CREDENTIAL TYPE <credential_type_name> USING <credential_of_ldap_account> ]
 [ USER LOOKUP URL <url_string_literal> ]
 [ NESTED GROUP LOOKUP URL { <url_string_literal> | NULL } ]
 [ ATTRIBUTE DN <dn_string_literal> ]
 [ ATTRIBUTE MEMBER_OF { <member_of_string_literal> | NULL } ]
 [ SSL { ON | OFF } ]
 [ DEFAULT { ON | OFF } ]
 [ { ENABLE | DISABLE } PROVIDER ]
 [ { ENABLE USER CREATION FOR LDAP <usertype_option> | DISABLE USER CREATION FOR
LDAP } ]
```

## Syntax Elements

#### ldap_provider_name

Specifies the identifier of a valid LDAP provider.

```sql
<ldap_provider_name> ::= <unicode_name>
```

#### CREDENTIAL TYPE credential_type_name USING credential_of_ldap_account

Specifies the credential type for the LDAP access account. Only one credential type can be configured for an LDAP provider and the only supported type is PASSWORD.

```sql
<credential_type_name> ::= 'PASSWORD'
<credential_of_ldap_account> ::=
'user=<user_dn_string_literal>;password=<passphrase>'
```

LDAP access account information includes the distinguished name (DN) and password of the user that is set up in LDAP server for use by SAP HANA server. This user must have permissions within the LDAP server to perform searches as specified by the USER LOOKUP URL and NESTED GROUP LOOKUP URL clauses.

PASSWORD specifies an LDAP access account for which you specify the credentials by using the USING clause.

`<credential_of_ldap_account>` specifies the credential of the LDAP access account that SAP HANA uses to log in to the LDAP server.

`<user_dn_string_literal>` specifies the distinguished name (DN) of the LDAP access account that HANA uses to log in to the LDAP server.

`<passphrase>` specifies the password for the access account that SAP HANA uses to log in to the LDAP server.

An example CREDENTIAL clause might look like this: `'PASSWORD' USING 'user=cn=LookupAccount,o=largebank.com;password=secret'`.

#### USER LOOKUP URL url_string_literal

Specifies an LDAP URL that locates a unique user entry in the LDAP server that corresponds to an SAP HANA user. The format of a USER LOOKUP URL is as follows:

```sql
ldap[s]://<hostname>:<port>/<base_dn>?<attributes>?<scope>?<filter>
```

A search filter `<filter>` uses the USER_NAME of the SAP HANA user to locate the user entry in the LDAP Server.`<filter>` must include a condition of the form `'<attr>=*'` where `<attr>` is an LDAP attribute whose value is matched against the USER_NAME of the SAP HANA user. SAP HANA replaces the `'*'` in the search filter with the USER_NAME of the current SAP HANA user

For example, when the following statement is executed, `(&(objectClass=user) (sAMAccountName=*))` is replaced with `(&(objectClass=user)(sAMAccountName=<USER_NAME of the current or specified SAP HANA user>))`:

```sql
USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))'
```

`<filter>` must contain one and only one `'*'`; otherwise, an error is returned..

The `<attributes>` specification lists LDAP attributes whose values are returned to the SAP HANA server for a given user entry. `<attributes>` must be left empty for USER LOOKUP URL. SAP HANA constructs the `<attributes>` internally based on the LDAP attributes specified with ATTRIBUTE clause.

The following is an example of a USER LOOKUP URL:

#### NESTED GROUP LOOKUP URL url_string_literal

Specifies an LDAP URL for obtaining LDAP group membership information, including nested groups, for a user from the LDAP server. For example: `NESTED GROUP LOOKUP URL 'ldap://myhostname:389/ ou=groupsOU,dc=x??sub?(member:1.2.840.113556.1.4.1941:=*)'`

The asterisk in `<url_string_literal>` is replaced by the user DN, which is obtained by using the USER LOOKUP URL.

Depending upon the NESTED GROUP LOOKUP URL, one or more levels of LDAP groups may be returned. It is possible to specify a URL that returns only one level of groups with NESTED GROUP LOOKUP URL. SAP HANA sends this LDAP query to the LDAP server for execution. Before sending the query, SAP HANA replaces '\*' in the NESTED GROUP LOOKUP URL with the DN of the user obtained from execution of USER LOOKUP URL.

While ATTRIBUTE MEMBER_OF and NESTED GROUP LOOKUP URL are both optional, if LDAP authorization is used and neither of these are defined, then an error is returned at run-time.

Support for nested LDAP groups is provided only when a single URL can be specified such that it returns a complete list of groups with the user’s membership (including groups with indirect membership). SAP HANA does not recursively fetch nested groups if they were not obtained by executing the search specified by NESTED GROUP LOOKUP URL.

#### ATTRIBUTE DN dn_string_literal

Specifies the LDAP attribute that provides the DN (distinguished name) of the LDAP User entry. The DN of the user is stored in the SAP HANA catalog.

#### ATTRIBUTE MEMBER_OF member_of_string_literal

Specifies or removes (NULL) the LDAP attribute that provides a list of groups that a user is a member of. If NESTED GROUP LOOOKUP URL is specified, then the group information is obtained using NESTED GROUP LOOKUP URL (that is, ATTRIBUTE MEMBER_OF is not used).

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

If you create multiple named LDAP providers, then you can designate one as the default. Designating an LDAP provider as DEFAULT removes the default designation of the previous default LDAP provider, if any.

#### {ENABLE | DISABLE } PROVIDER

Enables or disables the use of an LDAP provider. The default is DISABLE PROVIDER.

If a default LDAP provider is disabled, then users cannot log in by using LDAP authorization. VALIDATE LDAP PROVIDER can still be used to verify the configuration of a disabled LDAP provider.

#### { ENABLE | DISABLE } USER CREATION FOR ...

Enables or disables automatic user creation for LDAP authentication.

```sql
[ { ENABLE USER CREATION FOR LDAP [ <usertype_option> ] | DISABLE USER
CREATION FOR LDAP } ]
<usertype_option> ::= USER TYPE { STANDARD | RESTRICTED }
```

When enabling automatic user creation, optionally specify the type of the new users to be created. By default, new users are created as STANDARD users.

## Description

Use the ALTER LDAP PROVIDER statement to update the configuration of an LDAP provider:

If the LDAP provider is set to DEFAULT OFF and there is no other default provider that is enabled, or if the LDAP provider is set to DISABLE PROVIDER and there is no other default provider that is enabled, then:

- Any user connections created before the expiration of the value for the ldap_authorization_role_reuse_duration database property succeed.
- Any user connections created after the expiration of the value for the ldap_authorization_role_reuse_duration database property fail.
- Any first time user connections will fail.

When a default and enabled LDAP provider is altered such that it is either no longer a default LDAP provider or it is no longer enabled, the following occurs with respect to authentication and authorization:

- In case of authentication, the connection fails
- In case of authorization, the user connections may succeed. This is because within the user's role reuse duration, SAP HANA does not contact the LDAP server to validate the user's role with LDAP server.

## Permissions

Only users with the LDAP ADMIN privilege can alter LDAP providers.

## Examples

**Example 1:** Alter the USER LOOKUP URL for an LDAP provider called `my_ldap_provider`:

```sql
ALTER LDAP PROVIDER my_ldap_provider
  USER LOOKUP URL 'ldap://myhostname:389/ou=Users,dc=largebank,dc=com??sub?
(&(objectClass=user)(sAMAccountName=*))';
```

**Example 2:** Make the LDAP provider `my_ldap_provider` the default and enable it:

```sql
ALTER LDAP PROVIDER my_ldap_provider DEFAULT ON ENABLE PROVIDER;
```

**Example 3:** Change the NESTED GROUP LOOKUP URL for the LDAP provider `my_ldap_provider`:

```sql
ALTER LDAP PROVIDER my_ldap_provider
 NESTED GROUP LOOKUP URL 'ldap://myhostname:389/ou=groupsOU,dc=x?sub?(member:
1.2.840.113556.1.4.1941:=*)';
```

**Example 4:** Remove the NESTED GROUP LOOKUP URL setting for the LDAP provider`my_ldap_provider`, and add the ATTRIBUTE MEMBER_OF setting instead:

```sql
ALTER LDAP PROVIDER my_ldap_provider
 NESTED GROUP LOOKUP URL NULL
 ATTRIBUTE MEMBER_OF 'memberOf';
```

**Example 5:** Enable automatic user creation for LDAP authentication:

```sql
ALTER LDAP PROVIDER my_ldap_provider ENABLE USER CREATION FOR LDAP;
```

**Example 6:** Change the user type for the new users to be auto-created with LDAP authentication to RESTRICTED:

```sql
ALTER LDAP PROVIDER my_ldap_provider
  ENABLE USER CREATION FOR LDAP USER TYPE RESTRICTED;
```

**Example 7:** Disable user creation for LDAP authentication:

```sql
ALTER LDAP PROVIDER my_ldap_provider DISABLE USER CREATION FOR LDAP;
```

## Related Information

CREATE LDAP PROVIDER Statement (Access Control) [→](../CREATE-LDAP-PROVIDER-Statement-Access-Control.md) DROP LDAP PROVIDER Statement (Access Control) [→](../DROP-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](../VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_PROVIDER_URLS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDER_URLS-System-View.md) LDAP_PROVIDERS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDERS-System-View.md) LDAP_USERS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/LDAP_USERS-System-View.md)
