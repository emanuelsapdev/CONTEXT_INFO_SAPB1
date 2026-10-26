# 4.9.1.74 ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 183

Returns a value that indicates whether the root key backup password is set.

## Syntax

```sql
ENCRYPTION_ROOT_KEYS_HAS_BACKUP_PASSWORD()
```

## Description

Returns 1 if the password is already set or 0 if there is no password.

## Related Information

ALTER SYSTEM APPLICATION ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-APPLICATION-ENCRYPTION-Statement-System.md) ALTER SYSTEM BACKUP ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-BACKUP-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM LOG ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-LOG-ENCRYPTION-Statement-System-Management.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md)
