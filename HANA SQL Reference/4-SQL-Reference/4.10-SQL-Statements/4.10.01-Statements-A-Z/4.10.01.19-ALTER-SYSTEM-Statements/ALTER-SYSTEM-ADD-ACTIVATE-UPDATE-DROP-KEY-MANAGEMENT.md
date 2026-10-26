# 4.10.1.19.2 ALTER SYSTEM {ADD | ACTIVATE | UPDATE | DROP} KEY MANAGEMENT CONFIGURATION Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 469–470

Add, activate, update and drop key management configuration settings.

## Syntax

```sql
ALTER SYSTEM
ADD KEY MANAGEMENT CONFIGURATION <config_name> PROPERTIES '<settings>'
 | ACTIVATE KEY MANAGEMENT CONFIGURATION <config_name>
 | ALTER KEY MANAGEMENT CONFIGURATION <config_name> PROPERTIES '<updates>'
 | DROP KEY MANAGEMENT CONFIGURATION <config_name>
```

**config_name** Species a unique name consisting of uppercase letters only, for example, 'AWS_HSM'. The name 'DEFAULT' is forbidden.

#### settings

Creates a JSON document with key-value settings. The list of keys and their supported values depends on the chosen KMS or HSM. The command will fail if the specified settings do not work.

#### updates

Modifies a JSON document with the new key-value settings. The list of keys and their supported values depends on the chosen HSM or KMS. All settings not described in the update remain unchanged.

## Permissions

The use of this statement requires the DATABASE ADMIN and ENCRYPTION ROOT KEY ADMIN privileges.

## Description

This can be used to switch from the current local secure store (LSS) configuration to an external key management service (KMS) or hardware security module (HSM).
