# 4.10.1.19.60 ALTER SYSTEM START DATABASE Statement (Tenant Database Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 557–558

Starts the specified database.

## Syntax

```sql
ALTER SYSTEM START DATABASE <database_name> [ FROM FALLBACK SNAPSHOT ]
```

## Syntax Elements

#### database_name

Specifies the database to start.

```sql
<database_name> ::= <identifier>
```

#### FROM FALLBACK SNAPSHOT

Starts the tenant database using the fallback snapshot. This allows you to restore the tenant database to the state it was in when the fallback snapshot was created. For more information about fallback snapshots, see the SAP HANA Tenant Databases Guide.

## Permissions

You must have the DATABASE ADMIN or DATABASE START privilege to use this statement.

## Example

Start the my_database database.

```sql
ALTER SYSTEM START DATABASE my_database;
```

## Related Information

ALTER DATABASE Statement (Tenant Database Management) [→](../ALTER-DATABASE-Statement-Tenant-Database-Management.md) M_SNAPSHOTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SNAPSHOTS-System-View.md) M_DATABASES System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASES-System-View.md)
