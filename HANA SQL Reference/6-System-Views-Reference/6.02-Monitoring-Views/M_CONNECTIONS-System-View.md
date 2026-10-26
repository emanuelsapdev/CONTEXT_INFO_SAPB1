# 6.2.45 M_CONNECTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1686–1690

Provides detailed information on connections between a client and a database. Information includes: connection status, client information, connection type, and resource utilization.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction object ID. |
| START_TIME | TIMESTAMP | Displays the connected time. |
| IDLE_TIME | BIGINT | Displays the time that the connection is unused and idle in milliseconds. |
| CONNECTION_STATUS | VARCHAR(128) | Displays the connection status:<br>**RUNNING**<br>A statement is executing. **IDLE**<br>No statements are currently executing on this connection. **QUEUING**<br>The connection is currently queued. The status changes to RUNNING when it is dequeued (this depends on the system's re source consumption). **EMPTY**<br>A historic connection that is re moved after 1 hour. The removal time can be configured in `indexserver.ini [session] connection_history_life` `time = 60 # minutes`. |
| CLIENT_HOST | NVARCHAR(256) | Displays the host name of client machine. |
| CLIENT_IP | VARCHAR(45) | Displays the IP of client machine. |
| CLIENT_PID | BIGINT | Displays the client process ID. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| CONNECTION_TYPE | VARCHAR(128) | Displays the connection type. Connection types include: Remote, Local, History (remote), and History (local). |
| OWN | VARCHAR(5) | Displays the user's own connection. Re turns TRUE if it is your own connection and FALSE if it is not. |
| IS_HISTORY_SAVED | VARCHAR(5) | Deprecated. |
| MEMORY_SIZE_PER_CONNECTION | BIGINT | Displays the allocated memory size per connection in bytes. |
| AUTO_COMMIT | VARCHAR(5) | Displays the commit mode of the current transaction. Returns TRUE if the current connection is in auto-commit mode and FALSE if it is not. |
| LAST_ACTION | VARCHAR(128) | Displays the last action completed by the current connection. Actions include: ExecuteGroup, CommitTrans, AbortTrans, PrepareStatement, Close Statement, ExecutePrepared, Execu teStatement, FetchCursor, CloseCur sor, LobGetPiece, LogPutPiece, Lob Find, Authenticate, Connect, Disconnect, ExecQidItab, CursorFetchItab, In sertIncompleteItab, AbapStream, TxStartXA, and TxJoinXA. |
| CURRENT_STATEMENT_ID | VARCHAR(256) | Displays the current statement ID. |
| CURRENT_OPERATOR_NAME | VARCHAR(64) | Displays the current operator name. |
| FETCHED_RECORD_COUNT | BIGINT | Displays the sum of the record count fetched by select statements. |
| AFFECTED_RECORD_COUNT | BIGINT | Displays the sum of the record count af fected by DML/DDL statements, for example:<br> `INSERT/UPDATE/DELETE/REPLACE/CREATE TABLE ... LIKE ... WITHDATA/CREATE TABLE ...AS (SELECT ..)/IMPORT/EXPORT` |
| SENT_MESSAGE_SIZE | BIGINT | Displays the total size of messages sent by the current connection in bytes. |
| SENT_MESSAGE_COUNT | BIGINT | Displays the total message count sent by the current connection. |
| RECEIVED_MESSAGE_SIZE | BIGINT | Displays the total size of messages received by the current connection in bytes. |
| RECEIVED_MESSAGE_COUNT | BIGINT | Displays the total message count received by the current connection. |
| CREATOR_THREAD_ID | BIGINT | Displays the thread ID that created the current connection. |
| CREATED_BY | VARCHAR(256) | Displays the engine component that created the connections. These include: Session, Planning, Repository, CalcEn gine, Authentication, Table Exporter, Loader, LLVM, JSVM, IMS Search API, OLAP Engine, Mergedog, Ping Status, Name Server, Queue Server, SQL Stored Procedure, Authorization, Trex ViaDbsl from ABAP, HybridTable Reor ganizer, and Session external. |
| IS_ENCRYPTED | VARCHAR(5) | Displays whether or not the connection is encrypted with secure communication enabled (SSL enabled): TRUE/ FALSE. |
| AUTHENTICATION_METHOD | VARCHAR(48) | Displays the name of the authentication method used to authenticate the connection. |
| END_TIME | TIMESTAMP | Displays the time when the connection is closed for history connections. |
| PARENT_CONNECTION_ID | INTEGER | Displays the parent connection ID. |
| CLIENT_DISTRIBUTION_MODE | VARCHAR(128) | Displays the client distribution mode of the current connection (for example, [distribution] client_distribu tion_mode). |
| LOGICAL_CONNECTION_ID | INTEGER | Displays the logical connection ID in statement routing. |
| SOURCE_SITE_LOGICAL_CONNECTION_ID | INTEGER | Displays the logical connection ID of the origin site. |
| CURRENT_SCHEMA_NAME | NVARCHAR(256) | Displays the current schema name. |
| CURRENT_THREAD_ID | BIGINT | Displays the current executing thread ID. |
| PRIORITY | TINYINT | Displays the userspecified priority. |
| WORKLOAD_CLASS_NAME | NVARCHAR(256) | Displays the name of the effective work load class. |
| CURRENT_COLLATION_NAME | VARCHAR(16) | Displays the name of the current collation. |
| CLOSE_REASON | VARCHAR(32) | Displays the reason for the connection close. |
| SSL_VERSION | VARCHAR(16) | Displays the SSL/TLS protocol version.<br>The result is empty if the connection does not use SSL (IS_ENCRYTED) or if the SSL_VERSION contains the used SSL protocol version. |
| SSL_CIPHER | VARCHAR(64) | Displays the SSL cipher used for the connection.<br>The result is empty if SSL_CIPHER contains the used ciphersuite. |
| HAS_SSL_CLIENT_CERTIFICATE | VARCHAR(5) | Displays whether mutual authentication is enabled: TRUE/FALSE. TRUE indicates that the secure communication is enabled (SSL enabled) and the certificate of the client is validated. If not, FALSE is returned. |

## Related Information

M_CONNECTION_STATISTICS System View [→](M_CONNECTION_STATISTICS-System-View.md) CONNECT Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CONNECT-Statement-Session-Management.md)
