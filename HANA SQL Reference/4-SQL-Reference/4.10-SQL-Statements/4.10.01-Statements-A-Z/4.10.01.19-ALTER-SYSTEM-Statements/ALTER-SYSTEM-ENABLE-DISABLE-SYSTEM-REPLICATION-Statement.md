# 4.10.1.19.7 ALTER SYSTEM {ENABLE | DISABLE} SYSTEM REPLICATION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 477–478

Enables/disables an SAP HANA system to serve as an SAP HANA System Replication (HSR) primary site.

## Syntax

```sql
ALTER SYSTEM ENABLE SYSTEM REPLICATION <site_name>
| ALTER SYSTEM DISABLE SYSTEM REPLICATION [ FORCE ]
```

## Syntax Elements

#### site_name

Specifies a unique identifier describing the SAP HANA system that will act as the primary site. **FORCE** Disables system replication, even if there are secondary sites attached.

## Description

These statements are only supported in an on-premise SAP HANA system.

The ENABLE SYSTEM REPLICATION `<site_name>` syntax configures an SAP HANA system to serve as an HSR primary site.

The DISABLE SYSTEM REPLICATION syntax removes the HSR configuration from the SAP HANA system. The SAP HANA system continues running, but without system replication enabled. Specify FORCE when you want to disable HSR while secondary sites are still attached; otherwise, the statement fails if other sites are still attached.

These statements are equivalent to configuring HSR by using the hdbnsutil utility. For more information about setting up a system replication primary site, see the SAP HANA Administration Guide.

## Permissions

You must be in SYSTEMDB and have the SYSTEM REPLICATION ADMIN privilege to enable or disable system replication.

## Examples

The following example configures an SAP HANA system to serve as an HSR primary site and assigns the site name `mySite`:

```sql
ALTER SYSTEM ENABLE SYSTEM REPLICATION mySite;
```

The following example removes the HSR configuration from the SAP HANA system:

```sql
ALTER SYSTEM DISABLE SYSTEM REPLICATION;
```
