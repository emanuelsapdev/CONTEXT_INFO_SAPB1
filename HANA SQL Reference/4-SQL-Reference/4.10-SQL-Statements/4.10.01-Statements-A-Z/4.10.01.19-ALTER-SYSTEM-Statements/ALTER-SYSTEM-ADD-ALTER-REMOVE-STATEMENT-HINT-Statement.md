# 4.10.1.19.3 ALTER SYSTEM {ADD | ALTER | REMOVE} STATEMENT HINT Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 470–472

Adds, alters, or removes statement hints from the system to a specified query or statement hash.

## Syntax

```sql
ALTER SYSTEM { ADD | ALTER } STATEMENT HINT ( [ <hint_list> ] ) [ [ NO ]
OVERRIDE ] ] [ COMMENT <comment> ] FOR <statement_hint_target>
| ALTER SYSTEM REMOVE STATEMENT HINT [ ALL ] FOR <statement_hint_target>
```

## Syntax Elements

#### hint_list

Specifies a set of hints that are applied to the target query or statement_hash.

```sql
<hint_list> ::= <hint> [,... ]
```

#### statement_hint_target

Specifies the target of the hints to apply.

```sql
<statement_hint_target> ::= { <target_query> | STATEMENT HASH
<statement_hash> }
```

#### [ NO ] OVERRIDE

Specifies whether to use a hint override with `<statement_hint_target>`. When OVERRIDE is specified, the hints specified in `<hint_list>` override any hints specified in `<statement_hint_target>` (e.g, `SELECT * FROM myView WITH HINT (NO_CS_JOIN)`.

#### COMMENT comment

Specifies a comment to add to the STATEMENT_HINTS system view when `<hint_list>` is applied to `<statement_hint_target>`. **ALL** Removes all hints (userdefined and system from the system that are associated with the specified `<statement_hint_target>`. If ALL is not specified, then only the userdefined hints are removed. If ALL and `<statement_hash>` are specified, then user hints, system hints and the statement hash are removed. If `<statement_hash>` is specified without ALL, then the current user hints are replaced with the system hints.

## Description

In a statement hint entry, there are two kinds of hints: system and user. User hints are the hints added by users with the ADD STATEMENT HINT defined above. System hints are the hints provided by the system by default when the system is upgraded.

In the case of conflicts, for example if user hints are already specified in the system for the SQL statement to which the system hints will be applied during the system upgrade, then the user hints stay in the system and the system hints are kept for later usage.

In the case of `<hints_list>` conflicts, for example USE_OLAP_PLAN and NO_USE_OLAP_PLAN, all hints are added to the target query without precedence or conflict resolution. This may cause queries to incur undefined behavior. Behavior is dependent on the implementation of each hint, making the result of the query containing the conflicts undeterminable.

ADD STATEMENT HINT adds hints specified in the `<hints_list>` to the specified target query or statement hash as a key. Separate multiple hints on the `<hints_list>` by a comma.

REMOVE STATEMENT HINT removes statement hints from the system that match the specified target query or statement hash. If there are system hints, and the ALL option is not specified, then instead of removing the statement hints from the system, REMOVE STATEMENT HINT replaces the current user hints with the system hints. If the ALL option is specified, the statement removes the user hints and the system hints together with the specified SQL statement string. If ALL and `<statement_hash>` are specified, then user hints, system hints and the statement hash are removed. If `<statement_hash>` is specified without ALL, then the current user hints are replaced with the system hints.

Both commands (ADD and REMOVE) also evict all cached plans for the target SQL statements from the SQL Plan Cache.

## Example

This example adds the NO_CS_JOIN and NO_CS_UNION_ALL hints to the SELECT query.

```sql
ALTER SYSTEM ADD STATEMENT HINT (NO_CS_JOIN, NO_CS_UNION_ALL) FOR SELECT * FROM
AAA, BBB WHERE AAA.X = BBB.X;
```

This example alters the user hints associated with the specified SELECT statement, and specifies a comment.

```sql
ALTER SYSTEM ALTER STATEMENT HINT (NO_CS_JOIN) COMMENT 'AAA related join' FOR
SELECT * FROM AAA, BBB WHERE AAA.X = BBB.X;
```

This example specifies an overriding hint to use with the specified SELECT statement.

```sql
ALTER SYSTEM ALTER STATEMENT HINT (NO_CS_UNION_ALL) COMMENT 'AAA related join'
FOR SELECT * FROM AAA, BBB WHERE AAA.X = BBB.X WITH HINT (NO_CS_JOIN);
```

This example removes all user hints associated with the specified SELECT statement.

```sql
ALTER SYSTEM REMOVE STATEMENT HINT FOR SELECT * FROM AAA, BBB WHERE AAA.X =
BBB.X;
```

This example adds the NO_CS_JOIN hint to the statement hash 36896ef08346b8321f88449d5c5e97f8.

```sql
ALTER SYSTEM ADD STATEMENT HINT (NO_CS_JOIN) FOR STATEMENT HASH
'36896ef08346b8321f88449d5c5e97f8';
```

This example removes all user hints associated with the statement hash 36896ef08346b8321f88449d5c5e97f8.

```sql
ALTER SYSTEM REMOVE STATEMENT HINT FOR STATEMENT HASH
'36896ef08346b8321f88449d5c5e97f8';
```

This example removes all user and system hints and the statement hash 36896ef08346b8321f88449d5c5e97f8.

```sql
ALTER SYSTEM REMOVE STATEMENT HINT ALL FOR STATEMENT HASH
'36896ef08346b8321f88449d5c5e97f8';
```

## Related Information

ALTER SYSTEM {ENABLE | DISABLE} STATEMENT HINT Statement (System Management) [→](ALTER-SYSTEM-ENABLE-DISABLE-STATEMENT-HINT-Statement-System.md) STATEMENT_HINTS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/STATEMENT_HINTS-System-View.md)
