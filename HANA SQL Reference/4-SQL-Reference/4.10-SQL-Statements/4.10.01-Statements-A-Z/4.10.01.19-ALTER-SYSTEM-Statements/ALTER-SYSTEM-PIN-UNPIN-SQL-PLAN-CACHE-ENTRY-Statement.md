# 4.10.1.19.8 ALTER SYSTEM {PIN | UNPIN} SQL PLAN CACHE ENTRY Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 478–480

Provides a runtime mechanism to bind the target query and hints to the Hint Table to force the compilation of the target query with the hint.

## Syntax

```sql
ALTER SYSTEM PIN SQL PLAN CACHE ENTRY <plan_id> [ WITH HINT ( <hint_items> ) ]
 | ALTER SYSTEM PIN SQL PLAN CACHE ENTRY LIKE <plan_id> WITH HINT
( <hint_items> )
 | ALTER SYSTEM UNPIN SQL PLAN CACHE ENTRY [ LIKE ] <plan_id>
```

## Syntax Elements

#### plan_id

Specifies the identifier of the plan to be pinned.

```sql
<plan_id> ::= <integer_literal>
```

Refer to the M_SQL_PLAN_CACHE view to find the `<plan_id>` for the desired plan cache entry.

#### WITH HINT hint_items

Specifies one or more hints (comma-separated list) to apply to the query. Refer to the HINTS system view for list of available hint items.

```sql
<hint_items> ::= <string_literal>
```

Pinning a plan with a WITH HINT clause binds the target query to the HINT table.

#### PIN

PIN specifies to preserve a plan.

ALTER SYSTEM PIN...WITH HINT clause binds the target query to the HINT table.

ALTER SYSTEM PIN without a WITH HINT clause pins a plan to the SQL plan cache so that the pinned plan will not be evicted from the SQL plan cache, even after an ALTER SYSTEM CLEAR SQL PLAN CACHE is executed. SESSION LOCAL plans are pinned for the duration of the connection, and are evicted when the user connection is closed, regardless of its pin status

Pinned plans are returned to being normal plans after a restart. Only hints remain after a restart.

#### UNPIN

UNPIN reverts a pinned plan to a state where it may be evicted following the normal Last Recently Used (LRU) eviction scheme, as follows:

- If the plan was compiled with a WITH HINT clause and pinned to the plan cache (ALTER SYSTEM PIN...WITH HINT), then UNPIN removes the hint, unpins the plan, and the plan will be evicted as per the LRU scheme.
- If the plan was compiled without a WITH HINT clause and pinned (ALTER SYSTEM PIN), then the plan is unpinned and will be evicted as per the LRU scheme.

## Description

Refer to the PINNED_SQL_PLANS view to verify the list of currently pinned queries.

If you want to unpin a plan from the SQL plan cache but keep the hint info, you can run an ALTER SYSTEM ADD STATEMENT HINT statement after unpinning.

Check whether the hints in `<hint_items>` affect the query plan by using the EXPLAIN PLAN command with the `<plan_id>` parameter.

Typical pinning scenario:

1. Identify the problematic query from the system.
2. Try to append applicable hints to the query to find the target hint.
3. Look for the corresponding cache entry from the M_SQL_PLAN_CACHE view and identify the `<plan_id>`.
4. Bind the query and the hint using the ALTER SYSTEM PIN statement. Subsequent execution of the query should use the newly compiled/cached plan.

If WITH HINT is specified, then during indexserver start-up, pinned queries are restored using information from the PINNED_SQL_PLANS view. For each pair of SQL Plan Cache key and hints in the PINNED_SQL_PLANS view, a plan with the respective hint is compiled and inserted into the SQL Plan cache. If WITH HINT is not specified, then pinned plans are no longer pinned after an indexserver restart.

## Permissions

You must have the OPTIMIZER_ADMIN privilege to execute the statements listed in the syntax section.

You must have the OPTIMIZER_ADMIN or SYSTEM privilege to access the PINNED_SQL_PLANS view.

## Examples

The following statement pins a fictitious plan `20170203150455`:

```sql
ALTER SYSTEM PIN SQL PLAN CACHE ENTRY '20170203150455';
```

The following statement unpins the fictitious plan `20170203150455`:

```sql
ALTER SYSTEM UNPIN SQL PLAN CACHE ENTRY '20170203150455';
```

The following statement pins the fictitious plan `1000003`, and specifies the USE_OLAP_PLAN hint:

```sql
ALTER SYSTEM PIN SQL PLAN CACHE ENTRY '1000003' WITH HINT (USE_OLAP_PLAN);
```

## Related Information

EXPLAIN PLAN Statement (Data Manipulation) [→](../EXPLAIN-PLAN-Statement-Data-Manipulation.md) PINNED_SQL_PLANS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/PINNED_SQL_PLANS-System-View.md) HINTS System View [→](../../../../6-System-Views-Reference/6.01-System-Views/HINTS-System-View.md) M_SQL_PLAN_CACHE System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE-System-View.md)
