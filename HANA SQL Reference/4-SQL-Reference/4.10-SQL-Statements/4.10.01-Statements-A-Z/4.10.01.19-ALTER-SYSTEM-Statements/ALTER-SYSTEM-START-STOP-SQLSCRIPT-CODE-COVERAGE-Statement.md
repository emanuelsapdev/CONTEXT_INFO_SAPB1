# 4.10.1.19.59 ALTER SYSTEM {START | STOP} SQLSCRIPT CODE COVERAGE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 555–557

Starts and stops a SQLScript code coverage session for functions and procedures.

## Syntax

To start SQLScript code coverage:

```sql
ALTER SYSTEM START SQLSCRIPT CODE COVERAGE
 [ FOR DEBUG TOKEN <token_id> ]
 [ FOR USER <user_id> ]
 [ FOR APPLICATION USER <application_user_id> ]
 [ FOR SESSION <session_id> ]
```

To stop SQLScript code coverage:

```sql
ALTER SYSTEM STOP SQLSCRIPT CODE COVERAGE
```

## Syntax Elements

#### token_id

Specifies the token that the code coverage applies to.

#### user_id

Specifies the database user ID that the code coverage applies to.

#### application_user_id

Specifies the ID of the application user that the code coverage applies to.

#### session_id

Specifies the ID of the session that the code coverage applies to.

## Description

See the SAP HANA SQLScript Reference Guide for more information on code coverage support for functions and procedures in SQLScript.

SAP HANA stores the results of a code coverage session in the M_SQLSCRIPT_CODE_COVERAGE_RESULTS monitoring view and stores the definitions of objects that were used during a code coverage session in the M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS monitoring view.

Select from the monitoring views at any time, and from any column, you are interested in after starting code coverage. However, the full content of code coverage run is visible only after the query triggered in the second session (which is being covered) finishes (described in the second example, below).

The content in the monitoring views is overwritten in these views each time you stop a SQLScript code coverage session and start a new one. Since the data is temporary, copy or export the content from these views to retain data recorded by a SQLScript code coverage session before executing ALTER SYSTEM STOP SQLSCRIPT CODE COVERAGE.

You must have at least two connections for code coverage. In the first session you execute the codes on which you run code coverage, and in the second session you start the code coverage for a specific connection ID to record the coverage.

## Permissions

You must have the EXECUTE, DEBUG, and ATTACH_DEBUGGER privileges to perform code coverage.

## Example

SAP HANA requires two sessions to perform the code coverage. The examples below use session A to execute the code on which you run code coverage, and session B starts the code coverage for a specific connection ID to record the coverage.

1. In either session, create the `limitedLoop` and `dummy_proc` procedures:

```sql
CREATE PROCEDURE limitedLoop() AS
BEGIN
   DECLARE i BIGINT := 0;
    LOOP
      i := i + 1;
      IF :i > 27 THEN
            BREAK;
      END IF;
   END LOOP;
END;
CREATE PROCEDURE dummy_proc() AS
BEGIN
    SELECT * FROM DUMMY;
    CALL limitedLoop();
END;
```

2. From session A, issue this to determine the connection ID:

```sql
SELECT SESSION_CONTEXT('CONN_ID') FROM DUMMY;
```

3. In session B, start code coverage by using the connection ID of the user who is executing the code in session A (this example uses a connection ID of 203247):

```sql
ALTER SYSTEM START SQLSCRIPT CODE COVERAGE FOR SESSION '203247';
```

4. From session A, call the `dummy_proc` procedure:

```sql
CALL dummy_proc();
```

5. From session B, view the code coverage by querying the M_SQLSCRIPT_CODE_COVERAGE_RESULTS and M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS monitoring views

```sql
SELECT * FROM M_SQLSCRIPT_CODE_COVERAGE_RESULTS;
SELECT * FROM M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS;
```

If required, store the contents of the monitoring views for later reference (this can be a regular or a local temporary table):

```sql
CREATE LOCAL TEMPORARY TABLE "#SomeTableName" AS (SELECT * FROM
M_SQLSCRIPT_CODE_COVERAGE_RESULTS) WITH DATA;
```

6. From session B, disable the code coverage (this also clears the existing code coverage):

```sql
ALTER SYSTEM STOP SQLSCRIPT CODE COVERAGE;
```

## Related Information

CREATE PROCEDURE Statement (Procedural) [→](../CREATE-PROCEDURE-Statement-Procedural.md) CREATE FUNCTION Statement (Procedural) [→](../CREATE-FUNCTION-Statement-Procedural.md) M_SQLSCRIPT_CODE_COVERAGE_RESULTS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_CODE_COVERAGE_RESULTS-System-View.md) M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS System View [→](../../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS-System-View.md)
