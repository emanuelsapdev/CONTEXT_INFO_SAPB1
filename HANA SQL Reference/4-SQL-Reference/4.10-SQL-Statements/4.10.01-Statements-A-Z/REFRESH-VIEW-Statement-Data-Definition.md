# 4.10.1.132 REFRESH VIEW Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1019–1020

Refreshes an anonymized view.

## Syntax

```sql
REFRESH VIEW <anonymized_view_name> ANONYMIZATION
```

## Syntax Elements

#### anonymized_view_name

Specifies the name of the anonymized view to refresh.

## Description

You must refresh a view before you can select from it.

Refreshing a view can fail if privacy constraints cannot be satisfied due to the source data and parameters of the view. If this occurs, you can alter the view to adjust the constraints.

For more information on data anonymization, see the SAP HANA Administration Guide.

## Example

The following example refreshes a fictitious anonymized view called `Illness_K_Anon`:

```sql
REFRESH VIEW Illness_K_Anon ANONYMIZATION;
```

For a working example of how to refresh an anonymized view, see the anonymized view example found in the Examples section of the CREATE VIEW statement topic.

## Related Information

CREATE VIEW Statement (Data Definition) [→](CREATE-VIEW-Statement-Data-Definition.md) ALTER VIEW Statement (Data Definition) [→](ALTER-VIEW-Statement-Data-Definition.md) ANONYMIZATION_VIEWS System View [→](../../../6-System-Views-Reference/6.01-System-Views/ANONYMIZATION_VIEWS-System-View.md) ANONYMIZATION_VIEW_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/ANONYMIZATION_VIEW_COLUMNS-System-View.md)

[M_ANONYMIZATION_VIEWS System View](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_ANONYMIZATION_VIEWS-System-View.md)
