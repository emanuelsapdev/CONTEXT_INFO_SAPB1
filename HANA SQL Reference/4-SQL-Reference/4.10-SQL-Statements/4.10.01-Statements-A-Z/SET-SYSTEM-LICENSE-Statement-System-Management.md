# 4.10.1.149 SET SYSTEM LICENSE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1101–1103

Installs a license key to the database instance.

## Syntax

```sql
SET SYSTEM LICENSE <license_key>
```

## Syntax Elements

#### license_key

Specifies the license key.

```sql
<license_key> ::= <string_literal>
```

## Permissions

The LICENSE ADMIN system privilege is required to execute this command.

## Description

The license key (license key="") is copied and pasted from the license key file.

## Example

Set the system license with a license code. The license shown below does not contain a license key, so you cannot run this example.

```sql
SET SYSTEM LICENSE
 '----- Begin SAP License -----
 SAPSYSTEM=HD1
 HARDWARE-KEY=K4150485960
 INSTNO=0110008649
 BEGIN=20110809
 EXPIRATION=20151231
 LKEY=...
 SWPRODUCTNAME=SAP-HANA
 SWPRODUCTLIMIT=2147483647
 SYSTEM-NR=00000000031047460';
```
