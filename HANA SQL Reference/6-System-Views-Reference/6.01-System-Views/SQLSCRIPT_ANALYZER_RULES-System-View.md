# 6.1.152 SQLSCRIPT_ANALYZER_RULES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1571

Provides information regarding SQLScript Code Analyzer rules.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| RULE_NAMESPACE | VARCHAR(16) | Displays the namespace for the rule. |
| RULE_NAME | VARCHAR(64) | Displays the rule name. |
| CATEGORY | VARCHAR(16) | Displays the classification of the rule: security, consistency, performance, and so on. |
| SHORT_DESCRIPTION | NVARCHAR(256) | Displays the short description of the rule. |
| LONG_DESCRIPTION | NVARCHAR(5000) | Displays the long description containing the rule background. |
| RECOMMENDATION | NVARCHAR(5000) | Displays the recommendation on how to handle the rule. |
