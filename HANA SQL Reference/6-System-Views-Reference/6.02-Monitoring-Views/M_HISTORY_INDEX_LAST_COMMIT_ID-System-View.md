# 6.2.125 M_HISTORY_INDEX_LAST_COMMIT_ID System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1813

Provides the last commit ID of a history index for each session.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SESSION_ID | BIGINT | Displays the session ID. |
| SESSION_OWNER_VOLUME_ID | BIGINT | Displays the volume ID of this session. |
| LAST_COMMIT_ID | BIGINT | Displays the last commit ID of history index in this session. |

## Related Information

COMMIT Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/COMMIT-Statement-Transaction-Management.md) HISTORY COLUMN Option (Time Travel) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.03-HISTORY-COLUMN-Option-Time-Travel.md)
