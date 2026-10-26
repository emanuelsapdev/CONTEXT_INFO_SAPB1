# 4.10.1.160 VALIDATE USER Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1127–1129

Validates the credentials of a user in the current database.

## Syntax

```sql
VALIDATE USER { <user_name> PASSWORD <password> | WITH ASSERTION <assertion> }
```

## Syntax Elements

#### user_name

Specifies the identifier for the credentials being validated.

#### password

Specifies the password for the credentials being validated.

#### assertion

Specifies a valid ticket for a single-sign on service such as SAML, JWT, SAPLOGON.

## Description

VALIDATE USER can be used to validate the credentials for a user in the current database without causing a login using the credentials.

When validation fails, an error is returned indicating that authentication failed. The error does not indicate whether the failure is because `<user_name>` does not exist or because the specified `<password>` does not match the current password for `<user_name>`.

After successful validation, the user name can be found in the session variable VALIDATE_USER_NAME.

## Examples

The following example validates the credentials of user `JSmith` and returns a message indicating that the statement executed successfully (`JSmith` is a valid user):

```sql
CREATE USER JSmith PASSWORD shg8475ghh11;
VALIDATE USER JSmith PASSWORD shg8475ghh11;
```

The following example returns an error indicating that validation of user `T12345` failed. Although the error does not indicate whether it failed because the user name doesn't exist or whether the password is incorrect, you can see from the example that the reason is because the password specified in the VALIDATE USER statement doesn't match the user's password:

```sql
CREATE USER T12345 PASSWORD suelg75sjh;
VALIDATE USER T12345 PASSWORD shgi33shi;
```

The following example returns an error indicating that validation failed (because the user `BJones` has not been created in this example):

```sql
VALIDATE USER BJones PASSWORD 34875hgj75;
```

The following example uses a single-sign on ticket to validate a user, and returns an error message indicating that authentication failed (because the single-sign on ticket in this case is fictitious):

```sql
VALIDATE USER WITH ASSERTION
'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4
gRG9lIiwiYWRtaW4iOnRydWV9.TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ';
```
