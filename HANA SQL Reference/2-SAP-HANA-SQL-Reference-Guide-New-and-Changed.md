# 2 SAP HANA SQL Reference Guide (New and Changed)

> Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 21–24

SAP HANA Platform 2.0 SPS 05 introduces new and changed features for the SAP HANA SQL and System Views Reference

## SQL Statements (New and Changed)

**ALTER DATABASE Statement (Changed)** You can now add, activate, update, and drop key management configurations on tenant databases. ALTER DATABASE Statement (Tenant Database Management) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-DATABASE-Statement-Tenant-Database-Management.md)

#### ALTER SYSTEM {ADD | ACTIVATE | UPDATE | DROP} KEY MANAGEMENT CONFIGURATION

**Statement (New)** You can now add, activate, update, and drop key management configurations on the system database. ALTER SYSTEM {ADD | ACTIVATE | UPDATE | DROP} KEY MANAGEMENT CONFIGURATION Statement (System Management) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ADD-ACTIVATE-UPDATE-DROP-KEY-MANAGEMENT.md)

#### ALTER SYSTEM ALTER TABLE PLACEMENT Statement (Changed)

You can now define a sets of custom table placement location information using new ALTER SYSTEM ALTER TABLE PLACEMENT LOCATION `<custom_location_specification>` syntax. ALTER SYSTEM ALTER TABLE PLACEMENT Statement (System Management) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-TABLE-PLACEMENT-Statement-System.md), M_TABLE_PLACEMENT_LOCATIONS System View [→](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PLACEMENT_LOCATIONS-System-View.md), TABLE_PLACEMENT_LOCATIONS System View [→](6-System-Views-Reference/6.01-System-Views/TABLE_PLACEMENT_LOCATIONS-System-View.md)

#### ALTER SYSTEM { ADD | ALTER } STATEMENT HINT Statement (Changed)

You can now add or alter hints that override a hint found in the target query. You can also specify a comment to add to the STATEMENT_HINTS system view when the statement hints are applied. ALTER SYSTEM {ADD | ALTER | REMOVE} STATEMENT HINT Statement (System Management) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ADD-ALTER-REMOVE-STATEMENT-HINT-Statement.md), STATEMENT_HINTS System View [→](6-System-Views-Reference/6.01-System-Views/STATEMENT_HINTS-System-View.md)

#### ALTER TABLE Statement (Changed)

Use ONLINE mode for the LOB REORGANIZE clause to allow LOB reorganize operations that do not serialize with concurrent DML operations. ALTER TABLE Statement (Data Definition) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) **CREATE DATABASE Statement (Changed)** Creating a database now supports key management configuration. CREATE DATABASE Statement (Tenant Database Management) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-DATABASE-Statement-Tenant-Database-Management.md) **CREATE INDEX Statement (Changed)** You can now specify the load unit when creating an index. You can now create an index without serializing with concurrent DML operations. CREATE INDEX Statement (Data Definition) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-INDEX-Statement-Data-Definition.md)

#### CREATE REMOTE SOURCE Statement (Changed)

Smart data access remote sources now support the credential type JWT, which allows single sign-on using the JSON Web Token. CREATE REMOTE SOURCE Statement (Access Control) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-REMOTE-SOURCE-Statement-Access-Control.md)

#### CREATE / ALTER / DROP X509 PROVIDER Statements (New)

This syntax allows you to manage X.509 providers. CREATE X509 PROVIDER (Access Control) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-X509-PROVIDER-Access-Control.md), ALTER X509 PROVIDER (Access Control) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-X509-PROVIDER-Access-Control.md), DROP X509 PROVIDER (Access Control) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-X509-PROVIDER-Access-Control.md) Two new system views, X509_PROVIDERS and X509_PROVIDER_RULES, have been added. The X509_USER_MAPPINGS system view has an additional column, X509_PROVIDER_NAME.

#### DROP INDEX Statement (Changed)

[You can now drop an index without serializing with concurrent DML operations. DROP INDEX Statement (Data Definition)](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-INDEX-Statement-Data-Definition.md)

#### EXPORT Statement (Changed)

[You can now exclude remote table data in an export without having to use the CATALOG ONLY option. EXPORT Statement (Data Import Export)](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/EXPORT-Statement-Data-Import-Export.md)

#### GRANT and REVOKE Statements (behavior change)

Previously, when you granted or revoked the ALL PRIVILEGES schema-level privilege, all schema-level privileges were granted. Now, DEBUG, DEBUG MODIFY, and SQLSCRIPT LOGGING are not included in the set that is granted or revoked and must be granted or revoked separately. GRANT Statement (Access Control) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/GRANT-Statement-Access-Control.md), REVOKE Statement (Access Control) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md)

## SQL Functions (New and Changed)

## System Views (New and Changed)

**KEY_MANAGEMENT_CONFIGURATIONS (New)** Displays information about the existing key management configurations. KEY_MANAGEMENT_CONFIGURATIONS System View [→](6-System-Views-Reference/6.01-System-Views/KEY_MANAGEMENT_CONFIGURATIONS-System-View.md)

#### HOST_SERVICE_THREAD_SAMPLES System View

The collection interval has changed from 3600 seconds to 600 seconds.

#### M_TABLE_PERSISTENT_MEMORY_FILES System View (New)

[Displays the persistent memory file information of a specified table. M_TABLE_PERSISTENT_MEMORY_FILES System View](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PERSISTENT_MEMORY_FILES-System-View.md)

## Other Changes by Feature Name (New and Changed)

#### New SPATIAL_OUTPUT_REPRESENTATION session variable

[Specifies the output format of ST_Geometry and ST_Point. Session Variables](4-SQL-Reference/4.08-Session-Variables.md)

#### SQL support for the new Kernel Profiler

The Kernel Profiler collects information about CPU consumption and wait times, which can be helpful in support scenarios. ALTER SYSTEM {START | STOP | SAVE | CLEAR} KERNEL PROFILER Statement (System Management) [→](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-SAVE-CLEAR-KERNEL-PROFILER.md), M_KERNEL_PROFILER System View [→](6-System-Views-Reference/6.02-Monitoring-Views/M_KERNEL_PROFILER-System-View.md)

#### MAXIMUM_NUMBER_OF_TABLES_IN_STATEMENT

The default has changed to 0 (unlimited). However, you can now also configure a threshold using a new max_table_count_in_statement parameter in `indexserver.ini`. System Limitations [→](4-SQL-Reference/4.11-System-Limitations.md)

#### HINT Details (New and Changed)

[The ROUTE_BY and ROUTE_BY_CARDINALITY hints now can be used with projection views as well as tables. HINT Details](4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/4.10.01.144.01-HINT-Details.md)

The following new hints have been added:

##### HEX_TABLE_SCAN

Guides the optimizer to prefer HEX table scans over unique index searches.

##### NO_HEX_TABLE_SCAN

Guides the optimizer to avoid HEX table scans.

##### HEX_UNIQUE_INDEX_SEARCH

Guides the optimizer to prefer HEX unique index searches over table scans.

##### NO_HEX_UNIQUE_INDEX_SEARCH

Guides the optimizer to avoid HEX unique index searches.

##### HEX_LIMIT

Guides the optimizer to prefer HEX limits over top K sorts.

##### NO_HEX_LIMIT

Guides the optimizer to avoid HEX limits.

##### HEX_TOPK_SORT

Guides the optimizer to prefer HEX top K sorts over HEX limits.

##### NO_HEX_TOPK_SORT

Guides the optimizer to avoid HEX top K sorts.
