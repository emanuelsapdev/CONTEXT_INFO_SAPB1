# 4.10.1.41 COMMIT Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 682–683

Makes changes to the database permanent, or terminates a userdefined transaction.

## Syntax

```sql
COMMIT
```

## Description

The system supports transactional consistency that guarantees the current job to be either completely applied to the system or disposed of.

If a user wants to apply the current job to the system persistently, then the user should issue a COMMIT command. If a COMMIT command is issued and successfully processed, then any change on the system that the current transaction has done is applied to the system and the change is visible to other jobs that start later. A job that has already been committed a via COMMIT command cannot be reverted.

In a distributed system, a standard two-phase-commit protocol is complied. In the first phase, transaction coordinator consults every participant whether if it is ready to commit, and sends the result to the participants in the second phase. The COMMIT command only works with an autocommit-disabled session.

## Example

```sql
COMMIT;
```
