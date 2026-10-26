# 6.2.115 M_FEATURE_USAGE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1800–1802

Provides detailed feature usage statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| COMPONENT_NAME | VARCHAR(32) | Displays the component name. |
| FEATURE_NAME | VARCHAR(64) | Displays the feature name. |
| IS_DEPRECATED | VARCHAR(5) | When set to TRUE, displays if a feature is deprecated, otherwise it is FALSE. |
| OBJECT_COUNT | BIGINT(19) | Displays the counter tracking the number of artifacts that belong to the feature. For example, thenumber of existing history tables. |
| CALL_COUNT | BIGINT(19) | Displays the counter tracking the number of times the feature was used since the last start of the indexserver. For example, number of accesses to any history table. |
| LAST_TIMESTAMP | TIMESTAMP(27) | Displays the last point in time when the feature was used. By default, the value is deprecated if this configuration has not changed. |
| LAST_CONNECTION_ID | INTEGER(10) | Displays the connection ID of the last feature usage. By default, the value is deprecated if this configuration has not changed. |
| LAST_USER_NAME | VARCHAR(256) | Displays the database user of the last feature usage, for example, SAP `<SID>`. By default, the value is deprecated if this configuration has not changed. |
| LAST_APPLICATION_USER_NAME | VARCHAR(256) | Displays the application user of the last feature usage, for example, `<D-User>`. By default, the value is deprecated if this configuration has not changed. |
| LAST_APPLICATION_NAME | VARCHAR(256) | Displays the application name of the last feature usage. By default, the value is deprecated if this configuration has not changed. |
| LAST_APPLICATION_SOURCE | VARCHAR(256) | Displays the application source name and location of the last feature usage. By default, the value is deprecated if this configuration has not changed. |
| LAST_STATEMENT_ID | VARCHAR(20) | Displays the statement ID of the last feature usage. By default, the value is deprecated if this configuration has not changed. |
| LAST_STATEMENT_HASH | VARCHAR(32) | Displays the statement hash of the last feature usage. By default, the value is deprecated if this configuration has not changed. |

## Native Storage Extension Feature Monitoring

Native Storage Extension (NSE) feature usage statistics can be seen in M_FEATURE_USAGE monitoring view.

Under the component name NSE, object count for table, column , partition and index are shown.

> **Note**
>
> OBJECT_COUNT here indicates the number of objects (table, column, partition, index) which have load unit defined as page-loadable.

### Examples

TABLE

| **COMPONENT_NAME** | **FEATURE_NAME** | **IS_DEPRECATED** | **OBJECT_COUNT** | **OTHER COLUMNS** |
| --- | --- | --- | --- | --- |
| NSE | TABLE | FALSE | 10 | ? |
| COLUMN<br>**COMPONENT_NAME** | **FEATURE_NAME** | **IS_DEPRECATED** | **OBJECT_COUNT** | **OTHER COLUMNS** |
| NSE | COLUMN | FALSE | 12 | ? |

PARTITION

| **COMPONENT_NAME** | **FEATURE_NAME** | **IS_DEPRECATED** | **OBJECT_COUNT** | **OTHER COLUMNS** |
| --- | --- | --- | --- | --- |
| NSE | PARTITION | FALSE | 15 | ? |
| INDEX<br>**COMPONENT_NAME** | **FEATURE_NAME** | **IS_DEPRECATED** | **OBJECT_COUNT** | **OTHER COLUMNS** |
| NSE | INDEX | FALSE | 2 | ? |

## Related Information

[M_FEATURES System View](M_FEATURES-System-View.md)
