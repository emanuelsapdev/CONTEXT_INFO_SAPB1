# 6.2.319 M_TABLE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2093–2095

Returns the table runtime statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name to which the table belongs. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name to be counted. |
| INSERT_COUNT | BIGINT | Displays the count of INSERT statements for the table. |
| DELETE_COUNT | BIGINT | Displays the count of DELETE statements for the table. |
| UPDATE_COUNT | BIGINT | Displays the count of UPDATE statements for the table. |
| REPLACE_COUNT | BIGINT | Displays the count of REPLACE statements for the table. |
| MERGE_COUNT | BIGINT | Displays the count of MERGE INTO statements for the table. |
| SELECT_COUNT | BIGINT | Displays the count of SELECT statements for the table. |
| LAST_MODIFY_TIME | TIMESTAMP | Displays the timestamp when the last INSERT, UPDATE, DELETE, or REPLACE statement was executed. |
| LAST_SELECT_TIME | TIMESTAMP | Displays the timestamp when the last SELECT statement was executed. |

## Additional Information

- The M_TABLE_STATISTICS system view is not transactional; when a DML statement is rolled back, count values in the view remain unchanged.
- DML statements that do not result in changes to data still increment the DML counters for the relevant tables.
- DML-related counters and SELECT_COUNT are only applicable to user tables.
- Generally, when a single SELECT statement touches more than one table (regardless of whether results are returned from those tables), the SELECT_COUNTER for each table touched is incremented. However, SELECT statements that are subqueries do not increment the SELECT_COUNT counter for the tables referenced in the subquery. For example, a SELECT statement that is a subquery of an INSERT statement does not increment the SELECT_COUNT counter.
- Nested SELECT statements, for example in procedures, increment the SELECT counter, with one exception: for a SELECT statement in a calculation view, nested SELECT statements cannot increment the SELECT counter when nested SELECT statements are optimized.

This view has a resettable counterpart; you can see the values since the last reset in the M_TABLE_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_TABLE_STATISTICS_RESET;`.

## Related Information

M_TABLE_STATISTICS_RESET System View [→](M_TABLE_STATISTICS_RESET-System-View.md) CREATE STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md) REFRESH STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-STATISTICS-Statement-Data-Definition.md) ALTER STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STATISTICS-Statement-Data-Definition.md)
