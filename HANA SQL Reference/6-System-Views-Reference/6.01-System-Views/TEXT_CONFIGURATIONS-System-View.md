# 6.1.171 TEXT_CONFIGURATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1601–1602

Provides information about configurations and other resources for customizing text analysis and text mining.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema containing the resource. |
| NAME | NVARCHAR(256) | Displays the name of the resource. |
| TYPE | VARCHAR (16) | Displays the resource type: hdbtextcon fig (configuration), textdict (dictionary), textrule (ruleset), textminingconfig, and so on. |
| OWNER_NAME | NVARCHAR (256) | Displays the name of the resource owner. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the timestamp when the re source was created or last updated. |
| DATA | BLOB | Displays the resource content. |

## Related Information

Text Mining [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/README.md) Text Mining: TM_CATEGORIZE_KNN Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.01-Text-Mining-TM_CATEGORIZE_KNN-Function.md) Text Mining: TM_GET_RELATED_DOCUMENTS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.02-Text-Mining-TM_GET_RELATED_DOCUMENTS-Function.md) Text Mining: TM_GET_RELATED_TERMS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.03-Text-Mining-TM_GET_RELATED_TERMS-Function.md) Text Mining: TM_GET_RELEVANT_DOCUMENTS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.04-Text-Mining-TM_GET_RELEVANT_DOCUMENTS-Function.md) Text Mining: TM_GET_RELEVANT_TERMS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.05-Text-Mining-TM_GET_RELEVANT_TERMS-Function.md) Text Mining: TM_GET_SUGGESTED_TERMS Function [→](../../5-Additional-SAP-HANA-Contexts/5.04-Text-Mining/5.04.06-Text-Mining-TM_GET_SUGGESTED_TERMS-Function.md) M_TEXT_ANALYSIS_LANGUAGES System View [→](../6.02-Monitoring-Views/M_TEXT_ANALYSIS_LANGUAGES-System-View.md) M_TEXT_ANALYSIS_MIME_TYPES System View [→](../6.02-Monitoring-Views/M_TEXT_ANALYSIS_MIME_TYPES-System-View.md)
