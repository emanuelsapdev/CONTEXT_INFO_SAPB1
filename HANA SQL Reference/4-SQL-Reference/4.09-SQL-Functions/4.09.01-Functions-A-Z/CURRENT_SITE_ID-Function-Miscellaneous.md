# 4.9.1.56 CURRENT_SITE_ID Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 165–166

Returns the ID of the site that is calling the function. This function is primarily for use in SAP HANA System Replication (HSR).

## Syntax

```sql
CURRENT_SITE_ID()
```

## Description

Every site in an SAP HANA System Replication (HSR) environment has a site ID. Calling this function in an HSR system returns the ID of the site that is calling the function. Learning the site ID is useful when you are using forced routing.

When this function is called in a non-HSR system, 0 is returned.

Do not reference the DUMMY table in the FROM clause when calling the function. Instead, reference an actual table at the target location (for example, the `<sap_schema>`.SVERS table, which is the recommended table for an SAP NetWeaver ABAP environment).

This function returns the current site ID once for every row in the table you reference (that is, the same site ID, but once for each table row). It is therefore recommended that you specify TOP 1 when calling the function to return the current site ID only once. See the example for how to do this.

## Example

The following fictitious example returns the ID of the site that is executing the query:

```sql
SELECT TOP 1 CURRENT_SITE_ID() FROM mySchema.SVERS ( RESULT_LAG('hana_sr'));
```
