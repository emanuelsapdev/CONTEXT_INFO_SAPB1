# 6.1.73 FLEXIBLE_TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1491–1492

Provides information about available flexible tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| IS_RECLAIMABLE | VARCHAR(5) | Displays whether the garbage collection is enabled: TRUE/FALSE. |
| DEFAULT_DATA_TYPE_NAME | VARCHAR(16) | Displays the name of the default data type. |
| DEFAULT_LENGTH | INTEGER | Displays the length of the default data type. |
| DEFAULT_SCALE | INTEGER | Displays the scale of the default data type. |
| HAS_AUTO_DATA_TYPE_PROMOTION | VARCHAR(5) | Displays whether the automatic type promotion is enabled: TRUE/FALSE. |

## Related Information

ALTER SYSTEM RECLAIM FLEXIBLE TABLES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-FLEXIBLE-TABLES-Statement-System.md) TABLES System View [→](TABLES-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md)
