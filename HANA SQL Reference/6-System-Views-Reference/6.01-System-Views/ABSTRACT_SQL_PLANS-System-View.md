# 6.1.1 ABSTRACT_SQL_PLANS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1400–1403

Lists information about abstract SQL plans.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| QUERY_ID | BIGINT | Displays a number that uniquely identifies the abstract SQL query. |
| ABSTRACT_SQL_PLAN_ID | BIGINT | Displays a number that uniquely identifies each abstract SQL plan entry. |
| HOST | VARCHAR(64) | Displays the host name of the location where the abstract SQL plan was captured. |
| PORT | INTEGER | Displays the port number of the location where the abstract SQL plan was captured. |
| VOLUME_ID | INTEGER | Displays the ID of the volume where the abstract SQL plan was captured. |
| STATEMENT_STRING | NCLOB | Displays the target statement string. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for the STATEMENT_STRING column. |
| PLAN_KEY | NVARCHAR(5000) | Displays the key for the abstract SQL plan in JSON format.<br>These values can affect the generated query execution plans. |
| ABSTRACT_SQL_PLAN | NCLOB | Displays the abstract SQL plan in JSON format. For example:<br> `{"alp_rels":[{"alp_Rel":{"alias":"DUMMY", "alp_id":1,"enumerated_by":139,"field_names":[], "hash_partition_column":-2147483648,"input_size":1, "intermediate_alternative":false,"is_ap_injected":false,"is_esx_node":false, "is_view_cache":false,"join_table_name ":"NULL","locationName":"selibm57:36903", "locked":false,"logically_enumerated":false,"multi_container_id":-1, "output_column_size":1,"partition_search_ids":[],"physical_operator_type":22, "referenced_cols":[{"col":0}],"rel_id":1000000,"rel_type":6,"schema_name":"SYS", "table_name":"DUMMY","table_type":0,"trex_externalkey_pos":-2147483648, "trex_rel_id":-1,"trex_rowid_needed":false,"trex_rowid_pos":-2147483648, "used_cols":[{"col":0}]}},{"alp_Rel":{"alp_id":0,"child_rel_id":1, "enumerated_by":139,"intermediate_alternative":false,"is_esx_node":false, "locationName":"selibm57:36903","locked":false,"logically_enumerated":true, "output_column_size":0,"physical_operator_type":0, "project_col_aliases":[{"alias":"NULL"}],"project_col_labels ":[{"label":"DUMMY"}], "project_cols":[{"alp_Exp":{"col_id":0,"exp_type":0,"field_name":"DUMMY", "is_grouping_id":false,"is_table_key":false,"org_table_name":"DUMMY", "position":-1,"prefetch":false,"promoted_type":{"ftc":0,"length":-1,"scale":0}, "real_result_type":{"ftc":8,"length":1,"scale":0},"rel_id":1000000, "result_type":{"ftc":29,"length":1,"scale":0},"schema_name":"SYS", "table_name":"DUMMY"}}],"rel_type":3,"trex_rel_id":-1}}], "applied_migrator_set":["3.0","4.0","5.0"],"related_objects":[{"object_id":132355, "object_name":"SYS.DUMMY","object_type ":1,"object_version":1}, {"object_id":135526,"object_name":"DUMMY","object_type":7, "object_version":1}],"root_rel_id":0}` |
| RELATED_OBJECTS | NCLOB | Displays related object information for the captured abstract SQL plan. |
| ABSTRACT_SQL_PLAN_VERSION | NVARCHAR(5000) | Displays the abstract SQL plan version with applied migration information. |
| IS_ENABLED | VARCHAR(5) | Displays whether the abstract SQL plan will be used (TRUE) or not (FALSE). |
| IS_VALID | VARCHAR(5) | Displays whether the abstract SQL plan is valid (TRUE) or in valid (FALSE). |
| DETAILS | NCLOB | Displays additional information on the abstract SQL plan, including invalidation reasons. |
| LAST_ENABLE_TIME | TIMESTAMP | Displays the timestamp when the abstract SQL plan was added or last enabled. |
| LAST_ENABLE_USER | NVARCHAR(256) | Displays the ID of the user who added or last enabled the abstract SQL plan. |
| LAST_DISABLE_TIME | TIMESTAMP | Displays the timestamp when the abstract SQL plan was last disabled. |
| LAST_DISABLE_USER | NVARCHAR(256) | Displays the ID of the user who last disabled the abstract SQL plan. |
| CAPTURE_TIME | TIMESTAMP | Displays the timestamp when the abstract SQL plan was captured. |
| CAPTURE_USER | NVARCHAR(256) | Displays the ID of the user who captured the abstract SQL plan. |

## Related Information

ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-REMOVE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} CAPTURE ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-CAPTURE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-APPLY-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-UPDATE-ABSTRACT-SQL-PLAN-Statement-System.md) M_ABSTRACT_SQL_PLAN_OVERVIEW System View [→](../6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](../6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
