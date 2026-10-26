# 6.2.74 M_DATABASE_REPLICAS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1739–1740

Provides source and target information for databases involved in replication.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SOURCE_DATABASE_NAME | NVARCHAR(256) | Displays the name of the source data base. |
| SOURCE_SYSTEMDB_HOST | VARCHAR(64) | Displays the host of the source system database. |
| SOURCE_SYSTEMDB_PORT | INTEGER | Displays the source system database port. |
| TARGET_DATABASE_NAME | NVARCHAR(256) | Displays the name of the target data base. |
| TARGET_SYSTEMDB_HOST | VARCHAR(64) | Displays the target system database host. |
| TARGET_SYSTEMDB_PORT | INTEGER | Displays the target system database port. |
| REPLICATION_STATUS | VARCHAR(12) | Displays the aggregated replication status of the database services. |

## Related Information

M_DATABASE_REPLICA_STATISTICS System View [→](M_DATABASE_REPLICA_STATISTICS-System-View.md) M_DATABASE System View [→](M_DATABASE-System-View.md) M_DATABASES System View [→](M_DATABASES-System-View.md) CREATE DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-DATABASE-Statement-Tenant-Database-Management.md) ALTER DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-DATABASE-Statement-Tenant-Database-Management.md) RENAME DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-DATABASE-Statement-Tenant-Database-Management.md) DROP DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-DATABASE-Statement-Tenant-Database-Management.md)
