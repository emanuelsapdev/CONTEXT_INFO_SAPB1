# 6.1.37 COLLATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1442

Provides the list of collations that can be specified in an ORDER BY clause.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| COLLATION_NAME | VARCHAR(64) | Displays the supported collation names. |
| DESCRIPTION | VARCHAR(64) | Displays the language and region description for the collation. |

## Additional information

The presence of CI or AI at the end of a collation name indicates that the collation is case-insensitive or accent-insensitive, respectively (for example, FRENCH_AI).

## Related Information

AUTO_CORR Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/AUTO_CORR-Function-Aggregate.md) CROSS_CORR Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CROSS_CORR-Function-Aggregate.md) DFT Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/DFT-Function-Aggregate.md) FIRST_VALUE Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/FIRST_VALUE-Function-Aggregate.md) LAST_VALUE Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/LAST_VALUE-Function-Aggregate.md) NTH_VALUE Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/NTH_VALUE-Function-Aggregate.md) SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md) STRING_AGG Function (Aggregate) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/STRING_AGG-Function-Aggregate.md) Window Functions and the Window Specification [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.14-Window-Functions/README.md)
