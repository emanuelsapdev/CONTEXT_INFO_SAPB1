# 6.1.155 STRUCTURED_PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1573–1575

Provides information about available structured (analytic) privileges.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STRUCTURED_PRIVILEGE_ID | BIGINT | Displays the object ID of the structured privilege. |
| STRUCTURED_PRIVILEGE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the privilege. |
| STRUCTURED_PRIVILEGE_NAME | NVARCHAR(256) | Displays the name of the structured privilege. |
| RESTRICTION_TYPE | NVARCHAR(256) | Displays the type of restriction: CUBER ESTRICTION, ACTIVITYRESTRICTION, VALIDITYRESTRICTION, or DIMEN SIONRESTRICTION. |
| DIMENSION_ATTRIBUTE | NVARCHAR(256) | Displays the name of the dimension attribute. |
| FILTER_ID | BIGINT | Displays the number of filters needed to combine all operators/operands belonging to one filter. |
| FILTER_TYPE | VARCHAR(16) | Displays the type of filter: STATIC/ DYNAMIC. |
| NEGATED | VARCHAR(5) | Indicates whether the operator is negated in the filter: TRUE/FALSE. |
| OPERATOR | VARCHAR(16) | Displays the type of operator: CON TAINS PATTERN, BETWEEN, EQUAL, IN, LESS THAN, LESS EQUAL, GREATER THAN, or GREATER EQUAL. |
| OPERAND_ORDER | INTEGER | Displays the sequence of the operands per filter ID. |
| OPERAND | NCLOB | Displays the value that the operator is compared to. |

## Related Information

CREATE STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) ALTER STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) DROP STRUCTURED PRIVILEGE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STRUCTURED-PRIVILEGE-Statement-Access-Control.md) PRIVILEGES System View [→](PRIVILEGES-System-View.md) EFFECTIVE_STRUCTURED_PRIVILEGES System View [→](EFFECTIVE_STRUCTURED_PRIVILEGES-System-View.md)
