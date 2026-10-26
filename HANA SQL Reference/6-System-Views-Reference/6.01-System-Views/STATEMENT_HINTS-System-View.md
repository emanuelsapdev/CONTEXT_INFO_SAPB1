# 6.1.154 STATEMENT_HINTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1572–1573

Provides information about statement hints, including when they were last enabled and/or disabled and by whom.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for the STATEMENT_STRING column. |
| HINT_STRING | NVARCHAR(5000) | Displays the hint string. |
| SYSTEM_HINT_STRING | NVARCHAR(5000) | Displays the system hint string that conflicts with the existing userdefined hint string (if a statement has both a userdefined hint and a system hint associated with it, then only the user-defined hint is effective). |
| IS_ENABLED | VARCHAR(5) | Displays whether the hint is enabled. Possible values: TRUE/FALSE. |
| LAST_ENABLE_TIME | TIMESTAMP | Displays the timestamp for when the hint was last enabled. |
| LAST_ENABLE_USER | NVARCHAR(256) | Displays the user who enabled the hint. |
| LAST_DISABLE_TIME | TIMESTAMP | Displays the timestamp for when the hint was last disabled. |
| LAST_DISABLE_USER | NVARCHAR(256) | Displays the user who disabled the hint. |
| IS_OVERRIDE | NVARFCHAR(5) | Specifies TRUE if an override is speci fied for the target query (e.g., ALTER SYSTEM ADD STATEMENT HINT.. OVERRIDE...). |
| COMMENTS | NVARCHAR(5000) | Specifies comments configured for a statement hint (e.g., ALTER SYSTEM ADD STATEMENT HINT.. COMMENT `<comment>`..) |

## Related Information

HINTS System View [→](HINTS-System-View.md) HINT Details [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/4.10.01.144.01-HINT-Details.md) ALTER SYSTEM {ENABLE | DISABLE} STATEMENT HINT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-STATEMENT-HINT-Statement-System.md) ALTER SYSTEM {ADD | ALTER | REMOVE} STATEMENT HINT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ADD-ALTER-REMOVE-STATEMENT-HINT-Statement.md)
