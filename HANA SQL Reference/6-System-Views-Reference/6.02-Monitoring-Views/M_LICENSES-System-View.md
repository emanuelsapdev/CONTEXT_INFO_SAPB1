# 6.2.146 M_LICENSES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1848–1850

Provides information on all of the licenses (if any) that are installed on this system.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HARDWARE_KEY | VARCHAR(11) | Displays the hardware key of the SAP HANA installation. |
| SYSTEM_ID | VARCHAR(3) | Displays the system identifier (SID). |
| INSTALL_NO | VARCHAR(10) | Displays the installation number. |
| SYSTEM_NO | VARCHAR(18) | Displays the system number. |
| GLAS_APPLICATION_ID | VARCHAR(6) | Displays the license ID for the software product. |
| PRODUCT_NAME | VARCHAR(256) | Displays the name of the licensed software product, for example, SAP HANA. |
| PRODUCT_DESCRIPTION | NVARCHAR(256) | Displays the description of the licensed software product. |
| PRODUCT_LIMIT | BIGINT | Displays the allowed product usage as specified by the license in bytes, for example, main memory. |
| PRODUCT_LIMIT_DESCRIPTION | NVARCHAR(256) | Displays the description of the product usage to be measured and its unit. |
| PRODUCT_USAGE | BIGINT | Displays the peak product usage value during last 13 months, measured periodically, in bytes. |
| MEASUREMENT_INTERVAL | INTEGER | Displays the interval of license measurement, in hours. |
| FIRST_INSTALLATION_TIME | TIMESTAMP | Displays the date of the first installation of the license. |
| START_DATE | TIMESTAMP | Displays the start date of the validity period of the license. |
| EXPIRATION_DATE | TIMESTAMP | Displays the expiration date of the validity period of the license. |
| LAST_SUCCESSFUL_CHECK | TIMESTAMP | Displays the latest date on which the license was successfully checked and found valid. |
| PERMANENT | VARCHAR(5) | Displays TRUE if the license is permanent and FALSE if the license is temporary. |
| VALID | VARCHAR(5) | Indicates whether the license is valid or not: TRUE/FALSE. |
| ENFORCED | VARCHAR(5) | Indicates whether the license is a memory-enforced license or not: TRUE/ FALSE. |
| LOCKED_DOWN | VARCHAR(5) | Indicates whether the system is locked down due to license status: TRUE/ FALSE. |
| IS_DATABASE_LOCAL | VARCHAR(5) | Indicates whether the license is a local database local license: TRUE/FALSE. If FALSE, then the license is provided globally by the SystemDB. |

## Related Information

M_LICENSE System View [→](M_LICENSE-System-View.md) M_LICENSE_MEASUREMENTS System View [→](M_LICENSE_MEASUREMENTS-System-View.md) M_LICENSE_MEASUREMENT_STATISTICS System View [→](M_LICENSE_MEASUREMENT_STATISTICS-System-View.md) M_LICENSE_USAGE_HISTORY System View [→](M_LICENSE_USAGE_HISTORY-System-View.md) SET SYSTEM LICENSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-SYSTEM-LICENSE-Statement-System-Management.md) UNSET SYSTEM LICENSE ALL Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNSET-SYSTEM-LICENSE-ALL-Statement-System-Management.md)
