# 6.2.65 M_CS_NSE_ADVISOR System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1727–1728

Provides an SQL interface of the NSE Recommendation Engine and advice on changing the load unit (page/ column) for certain tables in the SAP HANA system, balancing out performance and memory – thus achieving a low total cost of ownership.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. When the recommendation level is not column, this field is not applicable and the value NULL is used. |
| PART_ID | INTEGER | Displays the table partition ID. When the recommendation level is not Partition, this field is not applicable, and the value is 0. |
| LOAD_UNIT | VARCHAR(7) | Displays the recommended load unit for this object: COLUMN/PAGE. |
| MEMORY_SIZE_IN_MAIN | BIGINT | Displays the memory consumption size, in bytes, per granularity of the object in main memory. If not LOADED, the value is 0 is used. |
| MAIN_PHYSICAL_SIZE | BIGINT | Displays the storage size, in bytes, per granularity of the object. |
| GRANULARITY | VARCHAR(10) | Displays the object level at which the recommendation for this table is given: TABLE, PARTITION, or COLUMN. |
