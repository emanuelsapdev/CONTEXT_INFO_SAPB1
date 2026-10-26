# 6.2.101 M_ES_EXPENSIVE_STATEMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1777–1778

Provides extended storage expensive statement information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction ID. |
| STATEMENT_ID | VARCHAR(20) | Displays the statement ID. |
| OPERATION | NVARCHAR(5000) | Displays the type of operation: PRE PARE, EXECUTE, FETCH, CLOSE, or ES OPERATION. |
| START_TIME | TIMESTAMP | Displays the statement start time. |
| DURATION_MICROSEC | BIGINT | Displays the statement duration in microseconds. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| RECORDS | BIGINT | Displays the number of records. |
