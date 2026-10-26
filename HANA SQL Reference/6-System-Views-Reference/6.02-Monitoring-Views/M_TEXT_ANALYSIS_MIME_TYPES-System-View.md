# 6.2.332 M_TEXT_ANALYSIS_MIME_TYPES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2109–2110

Provides a list of supported mime types.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| MIME_TYPE_NAME | VARCHAR(256) | Displays the name of the mime type. |
| MIME_TYPE_DESCRIPTION | NVARCHAR(256) | Displays the description of the mime type. |

## Related Information

M_TEXT_ANALYSIS_LANGUAGES System View [→](M_TEXT_ANALYSIS_LANGUAGES-System-View.md) MIMETYPE Function (Fulltext) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/MIMETYPE-Function-Fulltext.md) CREATE FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-FULLTEXT-INDEX-Statement-Data-Definition.md) SQL Error Codes [→](../../4-SQL-Reference/4.12-SQL-Error-Codes.md) FULLTEXT_INDEXES System View [→](../6.01-System-Views/FULLTEXT_INDEXES-System-View.md) Text Mining: TM_GET_RELEVANT_TERMS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.05-Text-Mining-TM_GET_RELEVANT_TERMS-Function.md) Text Mining: TM_GET_RELATED_DOCUMENTS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.02-Text-Mining-TM_GET_RELATED_DOCUMENTS-Function.md) Text Mining: TM_CATEGORIZE_KNN Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.01-Text-Mining-TM_CATEGORIZE_KNN-Function.md)
