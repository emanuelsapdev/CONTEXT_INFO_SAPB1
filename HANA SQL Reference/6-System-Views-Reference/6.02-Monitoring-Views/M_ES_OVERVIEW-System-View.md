# 6.2.103 M_ES_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1780–1781

Provides extended storage overview information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CATEGORY | VARCHAR(32) | Displays the main category type for which the parameters and values are displayed: GENERAL, BUFFERS, MEM ORY, STORAGE, DELTA, BACKUP, and VERSIONING. |
| NAME | VARCHAR(255) | Displays the name of the parameter provided in the VALUE column. |
| VALUE | VARCHAR(255) | Displays the value of the parameter. |

## Related Information

CREATE EXTENDED STORAGE Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/CREATE-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md) ALTER EXTENDED STORAGE Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/ALTER-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md) GRANT EXTENDED STORAGE ADMIN Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/GRANT-EXTENDED-STORAGE-ADMIN-Statement-Dynamic-Tiering.md) DROP EXTENDED STORAGE Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/DROP-EXTENDED-STORAGE-Statement-Dynamic-Tiering.md) CREATE TABLE Statement (Extended Store Table) [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/CREATE-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md) ALTER TABLE Statement (Extended Store Table) [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/ALTER-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md)
