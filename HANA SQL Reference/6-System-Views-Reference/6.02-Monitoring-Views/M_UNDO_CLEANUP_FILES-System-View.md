# 6.2.341 M_UNDO_CLEANUP_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2120–2121

Provides information about undo files and cleanup files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| TYPE | VARCHAR(16) | Displays the file type: UNDO, CLEANUP, or FREE. |
| TID | BIGINT | Displays the transaction ID. |
| PAGE_COUNT | BIGINT | Displays the page count. |
| RAW_SIZE | BIGINT | Displays the raw size in bytes. |
| CLEANUP_MARK | BIGINT | Displays the cleanup position mark. |
| NESTED_SESSION_ID | INTEGER | Displays the nested session ID. |
| NESTED_SESSION_PARENT_ID | INTEGER | Displays the nested session parent ID. |
| DEPENDENT_INDEX | INTEGER | Displays the dependent index during redo. |
| INDOUBT_FLAG | VARCHAR(5) | Displays the indoubt flag for distributed transaction: TRUE/FALSE. |
| TENTATIVE_PRECOMMIT_POSITION | BIGINT | Displays the tentative precommit position. |
| COMMIT_ID | BIGINT | Displays the commit ID. This value is -1 for non-committed transactions. |

## Additional Information

Each undo or cleanup file in the system is represented by one row in this view. Undo files contain information needed for transaction rollback. These files are removed on transaction end. If data is deleted but must still be accessible because of MVCC isolation, then the corresponding information is written to cleanup files..

At the end of the transaction, cleanup files are passed to history management. Garbage collection uses the cleanup files to finally remove data. Undo files and cleanup files may be cached and reused because of performance issues. Cached files are assigned the type FREE. Undo files for row store are assigned the type EXTERNALUNDO.

## Related Information

[M_GARBAGE_COLLECTION_STATISTICS System View](M_GARBAGE_COLLECTION_STATISTICS-System-View.md)
