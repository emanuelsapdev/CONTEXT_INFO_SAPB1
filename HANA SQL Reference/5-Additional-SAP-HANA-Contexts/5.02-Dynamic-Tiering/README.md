# 5.2 Dynamic Tiering

> [↑ 5 SQL Reference for Additional SAP HANA Contexts](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1213–1216

> **Caution**
>
> This guide contains syntax variations for different product contexts. These are handled as separate reference topics that have titles that announce the context in square brackets at the end of the title. The guide is also organized to keep reference topics together for a context. Always be sure you are using the SQL reference topic specific to your context.

ALTER AUDIT POLICY Statement [Dynamic Tiering] [→](ALTER-AUDIT-POLICY-Statement-Dynamic-Tiering.md)

Enables or disables an audit policy.

ALTER DATABASE Statement [Dynamic Tiering] [→](ALTER-DATABASE-Statement-Dynamic-Tiering.md)

Alters an existing database by adding or removing a dynamic tiering `esserver` service.

ALTER EXTENDED STORAGE Statement [Dynamic Tiering] [→](ALTER-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)

Lets you manage the extended storage space.

ALTER INDEX Statement (Multistore Table) [Dynamic Tiering] [→](ALTER-INDEX-Statement-Multistore-Table-Dynamic-Tiering.md)

Changes the storage type of an index on a multistore table.

ALTER STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](ALTER-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)

Alters the properties of a data statistics object.

ALTER STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](ALTER-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md)

Alters the properties of a data statistics object.

ALTER SYSTEM ALTER CONFIGURATION Statement [Dynamic Tiering] [→](5.02.07-ALTER-SYSTEM-ALTER-CONFIGURATION-DT/README.md)

Sets or removes configuration parameters in an ini file.

ALTER SYSTEM RECONFIGURE SERVICE Statement [Dynamic Tiering] [→](ALTER-SYSTEM-RECONFIGURE-SERVICE-Statement-Dynamic-Tiering.md)

Reconfigure a specified service by applying the current configuration parameters.

ALTER TABLE Statement (Extended Store Table) [Dynamic Tiering] [→](ALTER-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Changes the definition of an extended store table.

ALTER TABLE Statement (Multistore Table) [Dynamic Tiering] [→](ALTER-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md)

Alters the definition of a multistore table.

CALL CHECK_CATALOG Statement (Multistore Table) [Dynamic Tiering] [→](CALL-CHECK_CATALOG-Statement-Multistore-Table-Dynamic.md)

Performs consistency checks of metadata in both multistore and extended store tables, based on the actions you specify as arguments to the procedure call.

CALL CHECK_ES Statement (Extended Store Table) [Dynamic Tiering] [→](CALL-CHECK_ES-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Checks the validity of the current database in the extended store. Optionally, it corrects allocation problems for dbspaces or databases. CHECK_ES does not check a partitioned table if partitioned data exists in offline dbspaces.

CALL CHECK_TABLE_CONSISTENCY Statement (Multistore Table) [Dynamic Tiering] [→](CALL-CHECK_TABLE_CONSISTENCY-Statement-Multistore-Table.md)

Performs consistency check actions in the column store partition of a multistore table.

CALL ES_REBUILD_INDEX Statement (Multistore Tables) [Dynamic Tiering] [→](CALL-ES_REBUILD_INDEX-Statement-Multistore-Tables-Dynamic.md)

When you encounter reports or errors running the CHECK_ES extended store database consistency checker, or if an index fails to meet performance expectations, call this procedure to rebuild indexes for tables in extended storage, including extended store partitions of a multistore table.

CREATE AUDIT POLICY Statement [Dynamic Tiering] [→](CREATE-AUDIT-POLICY-Statement-Dynamic-Tiering.md)

Creates a new audit policy for extended tables.

CREATE EXTENDED STORAGE Statement [Dynamic Tiering] [→](CREATE-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)

Creates a new extended storage database, starts it, and registers it as an SAP HANA service.

CREATE INDEX Statement (Extended Store Table) [Dynamic Tiering] [→](CREATE-INDEX-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Creates an index on an extended store table column.

CREATE INDEX Statement (Multistore Table) [Dynamic Tiering] [→](CREATE-INDEX-Statement-Multistore-Table-Dynamic-Tiering.md)

Creates an index on a multistore table column.

CREATE STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](CREATE-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)

Creates data statistic objects that allow the query optimizer to make better decisions for query plans.

CREATE STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](CREATE-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md)

Creates data statistic objects that allow the query optimizer to make better decisions for query plans.

CREATE TABLE Statement (Extended Store Table) [Dynamic Tiering] [→](CREATE-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Creates a new extended store table in the extended storage.

CREATE TABLE Statement (Multistore Table) [Dynamic Tiering] [→](CREATE-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md)

Creates a new multistore table in the database.

DROP EXTENDED STORAGE Statement [Dynamic Tiering] [→](DROP-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)

Removes an existing extended storage configuration from the SAP HANA database.

DROP STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](DROP-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)

Drops userdefined data statistics objects that the query optimizer uses to make decisions for query plans.

DROP STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](DROP-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md)

Drops userdefined data statistics objects that the query optimizer uses to make decisions for query plans.

EXPORT Statement (Extended Store Table) [Dynamic Tiering] [→](EXPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Exports extended store tables, views, column views, synonyms, sequences, and procedures in CSV format.

EXPORT Statement (Multistore Table) [Dynamic Tiering] [→](EXPORT-Statement-Multistore-Table-Dynamic-Tiering.md)

Exports multistore tables, views, column views, synonyms, sequences, and procedures in CSV format.

GRANT EXTENDED STORAGE ADMIN Statement [Dynamic Tiering] [→](GRANT-EXTENDED-STORAGE-ADMIN-Statement-Dynamic-Tiering.md)

Grants the EXTENDED STORAGE ADMIN system privilege required to manage dynamic tiering and create extended storage.

IMPORT Statement (Extended Store Table) [Dynamic Tiering] [→](IMPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Imports catalog objects into an extended store table.

IMPORT Statement (Multistore Table) [Dynamic Tiering] [→](IMPORT-Statement-Multistore-Table-Dynamic-Tiering.md)

Imports catalog objects into a multistore table.

IMPORT FROM Statement (Extended Store Table) [Dynamic Tiering] [→](IMPORT-FROM-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Imports external data from a file into an existing extended store table.

IMPORT FROM Statement (Multistore Table) [Dynamic Tiering] [→](IMPORT-FROM-Statement-Multistore-Table-Dynamic-Tiering.md)

Imports external data from a file into existing extended storage partitions in a multistore table.

INSERT Statement (Extended Store Table) [Dynamic Tiering] [→](INSERT-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Adds a record to an extended store table.

INSERT Statement (Multistore Table) [Dynamic Tiering] [→](INSERT-Statement-Multistore-Table-Dynamic-Tiering.md)

MERGE DELTA Statement [Dynamic Tiering] [→](MERGE-DELTA-Statement-Dynamic-Tiering.md)

On a delta-enabled extended store or multistore table, MERGE DELTA triggers a merge of data from the delta dbspace to the user dbspace. When used in a multistore table, you can restrict a manual delta merge to just the default store partition or extended store partition of the multistore table.

REFRESH STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](REFRESH-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)

Refreshes data statistic objects that the query optimizer uses to make better decisions for query plans.

REFRESH STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](REFRESH-STATISTICS-Statement-Multistore-Table-Dynamic.md)

Refreshes data statistic objects that the query optimizer uses to make better decisions for query plans.

UPDATE Statement (Extended Store Table) [Dynamic Tiering] [→](UPDATE-Statement-Extended-Store-Table-Dynamic-Tiering.md)

Changes the values of the records of an extended store table.

UPDATE Statement (Multistore Table) [Dynamic Tiering] [→](UPDATE-Statement-Multistore-Table-Dynamic-Tiering.md)

Changes the values of the records of a multistore table.

Additional Syntax [Dynamic Tiering] [→](Additional-Syntax-Dynamic-Tiering.md)

SQL syntax that matches SAP HANA core syntax.

## Contenido de esta sección

- [5.2.1 ALTER AUDIT POLICY Statement [Dynamic Tiering]](ALTER-AUDIT-POLICY-Statement-Dynamic-Tiering.md)
- [5.2.2 ALTER DATABASE Statement [Dynamic Tiering]](ALTER-DATABASE-Statement-Dynamic-Tiering.md)
- [5.2.3 ALTER EXTENDED STORAGE Statement [Dynamic Tiering]](ALTER-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)
- [5.2.4 ALTER INDEX Statement (Multistore Table) [Dynamic Tiering]](ALTER-INDEX-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.5 ALTER STATISTICS Statement (Extended Store Table) [Dynamic Tiering]](ALTER-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)
- [5.2.6 ALTER STATISTICS Statement (Multistore Table) [Dynamic Tiering]](ALTER-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.7 ALTER SYSTEM ALTER CONFIGURATION Statement [Dynamic Tiering]](5.02.07-ALTER-SYSTEM-ALTER-CONFIGURATION-DT/README.md)
- [5.2.8 ALTER SYSTEM RECONFIGURE SERVICE Statement [Dynamic Tiering]](ALTER-SYSTEM-RECONFIGURE-SERVICE-Statement-Dynamic-Tiering.md)
- [5.2.9 ALTER TABLE Statement (Extended Store Table) [Dynamic Tiering]](ALTER-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.10 ALTER TABLE Statement (Multistore Table) [Dynamic Tiering]](ALTER-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.11 CALL CHECK_CATALOG Statement (Multistore Table) [Dynamic Tiering]](CALL-CHECK_CATALOG-Statement-Multistore-Table-Dynamic.md)
- [5.2.12 CALL CHECK_ES Statement (Extended Store Table) [Dynamic Tiering]](CALL-CHECK_ES-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.13 CALL CHECK_TABLE_CONSISTENCY Statement (Multistore Table) [Dynamic Tiering]](CALL-CHECK_TABLE_CONSISTENCY-Statement-Multistore-Table.md)
- [5.2.14 CALL ES_REBUILD_INDEX Statement (Multistore Tables) [Dynamic Tiering]](CALL-ES_REBUILD_INDEX-Statement-Multistore-Tables-Dynamic.md)
- [5.2.15 CREATE AUDIT POLICY Statement [Dynamic Tiering]](CREATE-AUDIT-POLICY-Statement-Dynamic-Tiering.md)
- [5.2.16 CREATE EXTENDED STORAGE Statement [Dynamic Tiering]](CREATE-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)
- [5.2.17 CREATE INDEX Statement (Extended Store Table) [Dynamic Tiering]](CREATE-INDEX-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.18 CREATE INDEX Statement (Multistore Table) [Dynamic Tiering]](CREATE-INDEX-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.19 CREATE STATISTICS Statement (Extended Store Table) [Dynamic Tiering]](CREATE-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)
- [5.2.20 CREATE STATISTICS Statement (Multistore Table) [Dynamic Tiering]](CREATE-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.21 CREATE TABLE Statement (Extended Store Table) [Dynamic Tiering]](CREATE-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.22 CREATE TABLE Statement (Multistore Table) [Dynamic Tiering]](CREATE-TABLE-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.23 DROP EXTENDED STORAGE Statement [Dynamic Tiering]](DROP-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md)
- [5.2.24 DROP STATISTICS Statement (Extended Store Table) [Dynamic Tiering]](DROP-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)
- [5.2.25 DROP STATISTICS Statement (Multistore Table) [Dynamic Tiering]](DROP-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.26 EXPORT Statement (Extended Store Table) [Dynamic Tiering]](EXPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.27 EXPORT Statement (Multistore Table) [Dynamic Tiering]](EXPORT-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.28 GRANT EXTENDED STORAGE ADMIN Statement [Dynamic Tiering]](GRANT-EXTENDED-STORAGE-ADMIN-Statement-Dynamic-Tiering.md)
- [5.2.29 IMPORT Statement (Extended Store Table) [Dynamic Tiering]](IMPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.30 IMPORT Statement (Multistore Table) [Dynamic Tiering]](IMPORT-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.31 IMPORT FROM Statement (Extended Store Table) [Dynamic Tiering]](IMPORT-FROM-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.32 IMPORT FROM Statement (Multistore Table) [Dynamic Tiering]](IMPORT-FROM-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.33 INSERT Statement (Extended Store Table) [Dynamic Tiering]](INSERT-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.34 INSERT Statement (Multistore Table) [Dynamic Tiering]](INSERT-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.35 MERGE DELTA Statement [Dynamic Tiering]](MERGE-DELTA-Statement-Dynamic-Tiering.md)
- [5.2.36 REFRESH STATISTICS Statement (Extended Store Table) [Dynamic Tiering]](REFRESH-STATISTICS-Statement-Extended-Store-Table-Dynamic.md)
- [5.2.37 REFRESH STATISTICS Statement (Multistore Table) [Dynamic Tiering]](REFRESH-STATISTICS-Statement-Multistore-Table-Dynamic.md)
- [5.2.38 UPDATE Statement (Extended Store Table) [Dynamic Tiering]](UPDATE-Statement-Extended-Store-Table-Dynamic-Tiering.md)
- [5.2.39 UPDATE Statement (Multistore Table) [Dynamic Tiering]](UPDATE-Statement-Multistore-Table-Dynamic-Tiering.md)
- [5.2.40 Additional Syntax [Dynamic Tiering]](Additional-Syntax-Dynamic-Tiering.md)
