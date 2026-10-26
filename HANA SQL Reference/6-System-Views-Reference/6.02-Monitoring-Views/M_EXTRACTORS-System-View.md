# 6.2.113 M_EXTRACTORS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1798–1799

Provides direct extractor connection (DXC) status information

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema where the DSO tables are generated. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the DSOspecific status table. |
| CLIENT | NVARCHAR(3) | Displays the ID of the client. |
| STATUS | VARCHAR(5) | Displays the general status overview: OK/ERROR. |
| REQUEST_ID | INTEGER | Displays the SID of the request used for activation. |
| ERROR_MESSAGE | NVARCHAR(5000) | Displays the message in case of an error. |
| PHASE | VARCHAR(32) | Displays the phase of the last running operation. |
| TIMESTAMP | TIMESTAMP | Displays the timestamp of the operation phase. |

## Related Information

[EXTRACT Function (Datetime)](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/EXTRACT-Function-Datetime.md)
