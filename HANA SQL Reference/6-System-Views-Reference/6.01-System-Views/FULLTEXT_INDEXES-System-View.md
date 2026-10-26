# 6.1.74 FULLTEXT_INDEXES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1492–1495

Provides information about fulltext indexes on table columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| INDEX_NAME | NVARCHAR(256) | Displays the name of the fulltext index. |
| INDEX_OID | BIGINT | Displays the object ID of the fulltext index. |
| LANGUAGE_COLUMN | NVARCHAR(256) | Displays the column name of the indexed table containing language indica tors for the indexed documents. |
| MIME_TYPE_COLUMN | NVARCHAR(256) | Displays the column name of the indexed table containing MIME type indi cators for the indexed documents. |
| LANGUAGE_DETECTION | NVARCHAR(256) | Displays the set of languages to be considered for automatic language detection. |
| FAST_PREPROCESS | VARCHAR(5) | Displays whether or not preprocessing is done with reduced functionality (for example, linguistic search is not available), which speeds up the indexing: TRUE/FALSE. |
| FUZZY_SEARCH_INDEX | VARCHAR(5) | Displays whether or not a fuzzy search is performed with an additional index (faster search, but higher memory consumption): TRUE/FALSE. |
| SEARCH_ONLY | VARCHAR(5) | Displays whether or not the text-attributes do not store any DAFs (it is not possible to retrieve the HTML-converted or original data from the text-attribute): TRUE/FALSE. If the text-attribute is a shadow attribute (created via CREATE FULLTEXT INDEX), the source-attribute containing the original data is not affected by this flag. |
| IS_EXPLICIT | VARCHAR(5) | Displays whether or not the index is an explicit fulltext index (created by CRE ATE FULLTEXT INDEX): TRUE/FALSE. |
| FLUSH_AFTER_DOCUMENTS | INTEGER | Displays the used to store change-tracking behavior of the fulltext index. |
| FLUSH_EVERY_MINUTES | INTEGER | Displays the data used to store the change-tracking behavior of the fulltext index in minutes. |
| CONFIGURATION | NVARCHAR(256) | Displays that an explicit configuration file can be specified, for example, to enable named entity extraction. |
| INTERNAL_COLUMN_NAME | NVARCHAR(512) | Displays the name of the internal text-attribute. This value is only set if the fulltext index was not created using the TEXT data type. |
| PHRASE_INDEX_RATIO | REAL | Displays the float between 0.0 and 1.0 which indicates how much memory the phrase index may use as a percentage of the memory size of the fulltext index. |
| TEXT_MINING | VARCHAR(5) | Displays whether or not the text mining capabilities are enabled on the indexed column: TRUE/FALSE. |
| TEXT_ANALYSIS | VARCHAR(5) | Displays whether or not an additional table is created that stores text analysis results: TRUE/FALSE. Normally, this parameter should be set to FALSE. |
| MIME_TYPE | NVARCHAR(256) | Displays the MIME type indicator for the indexed documents. |
| TOKEN_SEPARATORS | NVARCHAR(256) | Displays the characters used as token separators. |
| TEXT_MINING_CONFIGURATION | NVARCHAR(256) | Displays the configuration that is used for text mining. |
| TEXT_MINING_CONFIGURATION_OVERLAY | NVARCHAR(5000) | Displays the data used to override certain parameters from the configuration specified in TEXT_MINING_CONFIGURATION without changing the configuration itself. |
| COMPRESSION_LEVEL | TINYINT | Displays whether additional compression is applied to the fulltext index. A value of 0 means no compression and a value of 1 or larger means that compression is applied. The larger the value, the higher the compression. |

## Related Information

CREATE FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-FULLTEXT-INDEX-Statement-Data-Definition.md) ALTER FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-FULLTEXT-INDEX-Statement-Data-Definition.md) DROP FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-FULLTEXT-INDEX-Statement-Data-Definition.md) M_FULLTEXT_COLUMN_STATISTICS System View [→](../6.02-Monitoring-Views/M_FULLTEXT_COLUMN_STATISTICS-System-View.md) M_FULLTEXT_QUEUES System View [→](../6.02-Monitoring-Views/M_FULLTEXT_QUEUES-System-View.md) INDEXING_STATUS Function (Fulltext) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_STATUS-Function-Fulltext.md) INDEXING_ERROR_CODE Function (Fulltext) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_ERROR_CODE-Function-Fulltext.md) INDEXING_ERROR_MESSAGE Function (Fulltext) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_ERROR_MESSAGE-Function-Fulltext.md) INDEXES System View [→](INDEXES-System-View.md)
