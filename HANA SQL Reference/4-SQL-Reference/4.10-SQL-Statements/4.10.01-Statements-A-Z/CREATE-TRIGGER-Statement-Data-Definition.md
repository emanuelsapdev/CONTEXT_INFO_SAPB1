# 4.10.1.69 CREATE TRIGGER Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 827–842

Creates a trigger on a table or view.

## Syntax

```sql
CREATE [ OR REPLACE ] TRIGGER <trigger_name> <trigger_action_time>
<trigger_event_list>
   ON <subject_table_name>
   [ REFERENCING <transition_list> ]
   [ <for_each> ]
   [ <trigger_order_clause> ]
   [ ONLINE ]
      BEGIN
         [ <trigger_decl_list> ]
         [ <proc_handler_list> ]
         <trigger_stmt_list>
      END
```

## Syntax Elements

#### OR REPLACE

Replaces the definition of the trigger if it already exists. A CREATE OR REPLACE operation does not change the ID of the trigger, nor any privileges associated with it.

#### trigger_name

Specifies the name of the trigger to be created, with optional schema name.

```sql
<trigger_name> ::= [<schema_name>.]<identifier>

<schema_name> ::= <unicode_name>
```

#### trigger_action_time

Specifies when the trigger action should occur.

```sql
<trigger_action_time> ::=
 BEFORE
 | AFTER
 | INSTEAD OF
```

##### BEFORE

Specifies that the trigger is executed before the DML operation on a table.

##### AFTER

Specifies that the trigger is executed after the DML operation on a table.

##### INSTEAD OF

Specifies that the trigger is executed instead of the DML operation on a view.

A view with an INSTEAD OF trigger becomes updatable. An INSTEAD OF trigger is only allowed for SQL views, not for tables or column views.

UPDATE with FROM clause and REPLACE DML is not allowed when an INSTEAD OF trigger exists.

This option is not supported within the FOR EACH clause.

#### trigger_event_list

Specifies the data modification command that activates the trigger action.

```sql
<trigger_event_list> ::=
 <trigger_event>
 | <trigger_event_list> OR <trigger_event>

<trigger_event> ::=
 INSERT
 | DELETE
 | UPDATE [ [ EXCEPT ] OF <column_name_list> ]

<column_name_list> ::= <column_name> [ , <column_name>}...]

<column_name> ::= <identifier>
```

If `<column_name_list>` is provided with the UPDATE OF clause, then the UPDATE trigger only fires if a column specified in the list is updated. If `<column_name_list>` is provided with the UPDATE EXCEPT OF clause, then the UPDATE trigger is not fired if a column specified in the list is updated. The UPDATE trigger is fired regardless of the UPDATE EXCEPT OF clause if columns that are not specified in the list are updated together.

#### subject_table_name

Specifies the subject table or view name.

```sql
<subject_table_name> ::= <identifier>
```

#### REFERENCING transition_list

When a trigger transition variable is declared, the trigger can access records that are being changed by the DML triggering the trigger. For more information, see Transition variable [→](CREATE-TRIGGER-Statement-Data-Definition.md) and Transition table [→](CREATE-TRIGGER-Statement-Data-Definition.md).

##### transition_list

Specifies one or more transition list entries.

```sql
<transition_list> ::= <transition> [ , <transition>...]
```

##### transition

Specifies a transition variable or table variable.

```sql
<transition> ::= <transition_variable> | <transition_table>
```

##### transition_variable

During row-level trigger execution, `<trans_var_name>`.`<column_name>` represents a single record from the corresponding column that is being changed by the DML.

```sql
<transition_variable> ::= { OLD | NEW } ROW [ AS ] <trans_var_name>

<trans_var_name> ::= <identifier>
```

`<column_name>` is the target tables column name. Only a ROW trigger can use a transition variable.

##### transition_table

During statement-level trigger execution, `<trans_tab_name>` represents records being changed by the trigger DML as a table variable.

```sql
<transition_table> ::= { OLD | NEW } TABLE [ AS ] <trans_tab_name>

<trans_tab_name> ::= <identifier>
```

Only statement triggers can use a transition table.

##### OLD

Specifies that you can access the old row of the DML in the trigger. This is the row that is replaced by an update or a deleted old row. UPDATE triggers and DELETE triggers can have OLD ROW transition variables or OLD TABLE transition table variables.

##### NEW

Specifies that you can access the new record of the DML in the trigger. This is the row that is inserted or the new updated row.

UPDATE triggers and INSERT triggers can have NEW ROW transition variables or NEW TABLE transition table variables.

#### for_each

Specifies whether the trigger is called in a row-wise or statement-wise fashion.

```sql
<for_each> ::= FOR EACH { ROW | STATEMENT }
```

The default is ROW.

##### ROW

Specifies that a row-level trigger is used. This is fired once for each row affected by the triggering event.

##### STATEMENT

Specifies that a statement-level trigger is used. This is fired once for each triggering event. Both row-store and column-store tables support statement level triggers

#### trigger_order_clause

Specifies the order in which the triggers are executed.

```sql
<trigger_order_clause> ::= { FOLLOWS | PRECEDES <trigger_name_list> }
<trigger_name_list> ::= <trigger_name> [,...]
```

**FOLLOWS** Specifies that the trigger being created is fired after the specified triggers in `<trigger_name_list>`. **PRECEDES** Specifies that the trigger being created is fired before the specified triggers in `<trigger_name_list>`.

#### ONLINE

Applies an intentional exclusive lock (instead of an exclusive lock) before performing the operation. An intentional exclusive lock differs from the default lock (exclusive) because it allows concurrent DML and DDL related to the object to proceed, and will retry the operation until it can proceed.

ONLINE applies an intentional exclusive lock only if the auto commit mode for DDL statements is set to on. If the auto commit mode for DDL statement is not set to on, then an exclusive lock is still applied.

#### trigger_decl_list

Specifies the trigger declaration.

```sql
<trigger_decl_list> ::= DECLARE <trigger_decl> [ … ]
```

##### trigger_decl

Declares trigger variables or trigger conditions.

```sql
<trigger_decl> ::=
 <trigger_var_decl>
 | <trigger_condition_decl>
```

The declared variable can be used as a scalar value assignment or referenced in a trigger SQL statement.

##### trigger_var_decl

Specifies the trigger variable declaration.

```sql
<trigger_var_decl> ::=
 <var_name> [ CONSTANT ] <data_type> [ NOT NULL ]
[<trigger_default_assign>];
```

##### var_name

Specifies the identifier of the trigger variable.

```sql
<var_name> ::= <identifier>
```

##### CONSTANT

Specifies that you cannot change the variable during trigger execution.

##### data_type

Specifies the data type of the trigger variable.

```sql
<data_type> ::=
 DATE
 | TIME
 | SECONDDATE
 | TIMESTAMP
 | TINYINT
 | SMALLINT
 | INTEGER
 | BIGINT
 | SMALLDECIMAL
 | DECIMAL
 | REAL
 | DOUBLE
 | VARCHAR
 | NVARCHAR
 | ALPHANUM
 | SHORTTEXT
 | VARBINARY
 | BLOB
 | CLOB
 | NCLOB
 | TEXT
 | BINTEXT
```

##### trigger_default_assign

Specifies the default value of the trigger variable.

```sql
<trigger_default_assign> ::= { DEFAULT <expression> | <expression> }
```

##### trigger_condition_decl

Specifies the condition handler declaration.

```sql
<trigger_condition_decl> ::=
 <condition_name> CONDITION;
 | <condition_name> CONDITION FOR <sql_error_code>;
```

##### condition_name

Specifies a declared condition name that you can reference in an exception handler.

```sql
<condition_name> ::= <identifier>
```

##### sql_error_code

Specifies the error code for exception handling.

```sql
<sql_error_code> ::= SQL_ERROR_CODE <int_const>
```

#### proc_handler_list

Declares exception handlers to catch SQL exceptions.

```sql
<proc_handler_list> ::= <proc_handler> [ <proc_handler> […] ]

<proc_handler> ::=
 DECLARE EXIT HANDLER FOR <proc_condition_value_list> <trigger_stmt>
```

##### proc_condition_value_list

Specifies one or more condition values.

```sql
<proc_condition_value_list> ::=
 <proc_condition_value> [,...]
```

##### proc_condition_value

Specifies a procedure condition value.

```sql
<proc_condition_value> ::=
 SQLEXCEPTION
 | SQLWARNING
 | <sql_error_code>
 | <condition_name>
```

You can use a specific error code number or condition name declared on a condition variable.

#### trigger_stmt_list

Specifies that the trigger body syntax is a subset of the procedure body syntax.

```sql
<trigger_stmt_list> ::= <trigger_stmt> [ <trigger_stmt> […] ]

<trigger_stmt> ::=
 <proc_block>
 | <proc_assign>
 | <proc_if>
 | <proc_loop>
 | <proc_while>
 | <proc_for>
 | <proc_foreach>
 | <proc_signal>
 | <proc_resignal>
 | <trigger_sql>
 | <trigger_proc_call>
 | <proc_exit>
 | <proc_continue>
 | <proc_open>
 | <proc_fetch>
 | <proc_close>
 | <proc_return>
```

For more information, see the CREATE PROCEDURE statement.

##### proc_block

Specifies sections of your trigger procedures that can be nested using BEGIN and END terminals.

```sql
<proc_block> ::=
 BEGIN
   [ <trigger_decl_list> ]
   [ <proc_handler_list> ]
   <trigger_stmt_list>
  END;
```

##### proc_assign

Assigns values to variables.

```sql
<proc_assign> ::= <var_name> := <expression>;

<var_name> ::= <identifier>
```

##### proc_if

Controls execution flow with conditionals.

```sql
<proc_if> ::=
 IF <condition> THEN <trigger_stmt_list> [ <proc_elsif_list> ]
[ <proc_else> ]
   END IF;
<proc_elsif_list> ::= <proc_elsif> [ <proc_elsif> […] ]
<proc_elsif> ::=
 ELSEIF <condition> THEN <trigger_stmt_list>
<proc_else> ::= ELSE <trigger_stmt_list>
```

##### condition

Specifies the conditions where the command should be performed.

```sql
<condition> ::=
 <condition> OR  <condition>
 | <condition> AND <condition>
 | NOT <condition>
 | ( <condition> )
 | <predicate>
```

##### proc_loop

Repeatedly executes a set of trigger statements.

```sql
<proc_loop> ::=
   LOOP
      <trigger_stmt_list>
   END LOOP;
```

##### proc_while

Repeatedly calls a set of trigger statements while a condition is true.

```sql
<proc_while> ::=
   WHILE
     <condition>
     DO <trigger_stmt_list>
   END WHILE;
```

##### proc_for

Iterates over a set of data.

```sql
<proc_for> ::=
 FOR <column_name> IN [ <reverse> ] <expression> [ <expression> […] ]
   DO <trigger_stmt_list>
  END FOR;
```

##### column_name

Specifies the name of the column where the data iteration is to occur.

```sql
<column_name> ::= <identifier>
```

##### reverse

Specifies that the results should be iterated over in reverse order.

```sql
<reverse> ::= REVERSE
```

##### proc_foreach

Iterates over all elements in a set of data.

```sql
<proc_foreach> ::=
 FOR <column_name> AS <column_name> [<open_param_list>]
   DO <trigger_stmt_list>
  END FOR;
```

##### open_param_list

Specifies one or more input expressions to be iterated over.

```sql
<open_param_list> ::= ( <expr_list> )
<expr_list> ::= <expression>[, <expression> [,…] ]
```

##### proc_signal

Explicitly raises an exception from within your trigger procedures.

```sql
<proc_signal> ::=
 SIGNAL <signal_value> [ <set_signal_info> ];
```

##### proc_resignal

Raises an exception on the action statement in an exception handler.

```sql
<proc_resignal> ::=
 RESIGNAL [<signal_value>] [ <set_signal_info> ];
```

If an error code is not specified, then RESIGNAL throws the caught exception.

##### signal_value

Specifies to SIGNAL or RESIGNAL a signal name or an SQL error code.

```sql
<signal_value> ::= { <signal_name> | <sql_error_code> }

<signal_name> ::= <identifier>

<sql_error_code> ::= <unsigned_integer>
```

##### set_signal_info

Delivers an error message to users when specified error is thrown during trigger execution.

```sql
<set_signal_info> ::= SET MESSAGE_TEXT = '<message_string>'
<message_string> ::= <any_character>
```

##### trigger_sql

Specifies the trigger SQL.

```sql
<trigger_sql> ::= <select_into_stmt>
 | <insert_stmt>
 | <delete_stmt>
 | <update_stmt>
 | <replace_stmt>
 | <upsert_stmt>
```

For information on `<insert_stmt>`, see the INSERT statement.

For information on `<delete_stmt>`, see the DELETE statement.

For information on `<update_stmt>`, see the UPDATE statement.

For information on `<replace_stmt>` and `<upsert_stmt>`, see the REPLACE | UPSERT statement.

##### select_into_stmt

```sql
<select_into_stmt> ::=
 SELECT <select_list> INTO <var_name_list> <from_clause>
   [ <where_clause> ]
   [ <group_by_clause> ]
   [ <having_clause> ]
   [ { <set_operator> <subquery> [, ... ] ]
   [ <order_by_clause> ]
   [ <limit> ]
```

##### trigger_proc_call

Calls a previously defined procedure.

```sql
<trigger_proc_call> ::= CALL <procedure_name>
```

The called procedure can only include SQL statements that are suitable for triggers.

For information on `<select_list>`, `<from_clause>`, `<where_clause>`, `<group_by_clause>`, `<having_clause>`, `<set_operator>`, `<subquery>`, `<order_by_clause>`, and `<limit>`, see the SELECT statement.

##### var_name_list

Specifies a scalar variable.

```sql
<var_name_list> ::= <var_name>[, <var_name> [,…] ]

<var_name> ::= <identifier>
```

You can assign a selected item value to this scalar variable.

##### proc_exit

Terminates a loop.

```sql
<proc_exit> ::= BREAK;
```

##### proc_continue

Skips current loop iteration and continues with the next value.

```sql
<proc_continue> ::= CONTINUE;
```

##### proc_open

Specifies cursor operations.

```sql
<proc_open> ::= OPEN <cursor_name> [ <open_param_list> ];
<proc_fetch> ::= FETCH <cursor_name> INTO <column_name_list>;
<proc_close> ::= CLOSE <cursor_name>;
```

##### proc_return

Returns from a trigger.

```sql
<proc_return> ::= RETURN;
```

Cannot return a value.

## Description

A trigger is a kind of procedure that automatically executes when an event occurs on a given table or view. The body of a trigger contains a set of statements that are executed when a given operation (INSERT/UPDATE/ DELETE) takes place on a given subject table or subject view.

The following notes apply to triggers:

- Referencing an associated column in the trigger is not allowed because the trigger transition table only has the subject table data in context during the operation.
- In the case of batch/bulk statements, a statement-level trigger is executed once per batch entry. So for example, if inserting a batch, then the statement-level trigger is executed for every INSERT statement entry in the batch.
- Statement-level triggers are supported for both row-store and column-store tables. You can convert a row table with a statement trigger into a column table by using ALTER TABLE.
- Modification (any INSERT/UPDATE/DELETE/REPLACE) of a subject table that a trigger is defined on is not allowed in the trigger body.
- A trigger on a partitioned table cannot access the subject table, while a trigger on a non-partitioned table can execute a SELECT statement on its subject table.
- When a subject table is accessed in a trigger body, batch updates do not always show row-wise results for performance reasons.
- The maximum trigger number per single table and per DML is 1024, which means a table can have maximum 1024 INSERT triggers, 1024 UPDATE triggers, and 1024 DELETE triggers in the same time.
- Most procedures are allowed in the body of a trigger. The procedure that is called in a trigger only can have SQL statements which are suitable for a trigger body.
- Transition variable modifications are allowed in the BEFORE trigger. Internal columns ($trexkey$, $rowid$, concat column) or generated column modifications are not allowed.
- Unsupported trigger actions:
  - Result-set assignments, such as selecting a result set assignment into a table type
  - Dynamic SQL execution, such as building SQL statements dynamically at SQLScript runtime

## Permissions

Only database users with the TRIGGER privilege for the given `<subject_table_name>` are allowed to create a trigger for that table or view.

## Examples

### Basic trigger usage

Create a table that the trigger is created for.

```sql
CREATE ROW TABLE TARGET ( A INT);
```

Create a table that the trigger accesses and modifies.

```sql
CREATE ROW TABLE SAMPLE ( A INT);
```

Create the following trigger.

```sql
CREATE TRIGGER TEST_TRIGGER
 AFTER INSERT ON TARGET FOR EACH ROW
 BEGIN
     DECLARE SAMPLE_COUNT INT;
     SELECT COUNT(*) INTO SAMPLE_COUNT FROM SAMPLE;
     IF :SAMPLE_COUNT = 0
     THEN
       INSERT INTO SAMPLE VALUES(5);
     ELSEIF :SAMPLE_COUNT = 1
     THEN
       INSERT INTO SAMPLE VALUES(6);
     END IF;
 END;
```

TEST_TRIGGER is executed after any record insert execution for TARGET table.

```sql
INSERT INTO TARGET VALUES (1);
 SELECT * FROM SAMPLE;
```

The SAMPLE table record count is zero at the first insert attempt and the trigger TEST_TRIGGER inserts 5 into the SAMPLE table. The SELECT statement returns 5.

```sql
INSERT INTO TARGET VALUES (2);
 SELECT * FROM SAMPLE;
```

On the second insertion to the TARGET table, the trigger inserts 6 into the SAMPLE table because its count is now two. The SELECT statement returns 6.

### Trigger ordering

Create the trigger TRIGGER_TEST_1 that is executed after an insert execution on TARGET table. TRIGGER_TEST_1 is executed following the execution of TEST_TRIGGER.

```sql
CREATE TRIGGER TRIGGER_TEST_1
AFTER INSERT ON TARGET
FOR EACH ROW FOLLOWS TEST_TRIGGER
BEGIN
     DECLARE SAMPLE_COUNT INT;
     SELECT COUNT(*) INTO SAMPLE_COUNT FROM SAMPLE;
     IF :SAMPLE_COUNT = 0
     THEN
       INSERT INTO SAMPLE VALUES(5);
     ELSEIF :SAMPLE_COUNT = 1
     THEN
       INSERT INTO SAMPLE VALUES(6);
     END IF;
 END;
```

### Trigger with AFTER UPDATE and a WHILE loop

```sql
CREATE ROW TABLE TARGET ( A INT);
 CREATE ROW TABLE SAMPLE ( A INT);
 CREATE TRIGGER TEST_TRIGGER_WHILE_UPDATE
 AFTER UPDATE ON TARGET
 BEGIN
     DECLARE found INT := 1;
     DECLARE val INT := 1;
     WHILE :found <> 0 DO
         SELECT count(*) INTO found FROM sample WHERE a = :val;
         IF :found = 0 THEN
             INSERT INTO sample VALUES(:val);
         END IF;
         val := :val + 1;
     END WHILE;
 END;
```

### UPDATE trigger with column list

```sql
CREATE ROW TABLE TARGET ( A INT, B INT);
CREATE ROW TABLE SAMPLE ( A INT);
CREATE TRIGGER TEST_TRIGGER_UPDATE_COLUMN_LIST
AFTER UPDATE OF B ON TARGET
BEGIN
    INSERT INTO SAMPLE VALUES(1);
END;
INSERT INTO TARGET VALUES(1, 1);
UPDATE TARGET SET A = 0;
 -- does not fire the trigger
SELECT COUNT(*) FROM SAMPLE;
```

The SELECT statement returns 0.

```sql
UPDATE TARGET SET B = 0; -- does fire the trigger
SELECT COUNT(*) FROM SAMPLE;
```

The SELECT statement returns 1.

### UPDATE EXCEPT OF trigger with column list

```sql
CREATE ROW TABLE TARGET ( A INT, B INT);
CREATE ROW TABLE SAMPLE ( A INT);
CREATE TRIGGER TEST_TRIGGER_UPDATE_EXCEPT_OF_COLUMN_LIST
AFTER UPDATE EXCEPT OF B ON TARGET
BEGIN
    INSERT INTO SAMPLE VALUES(1);
END;
INSERT INTO TARGET VALUES(1, 1);
UPDATE TARGET SET B = 0; -- does not fire the trigger
SELECT COUNT(*) FROM SAMPLE;
```

The SELECT statement returns 0.

```sql
UPDATE TARGET SET A = 0; -- does fire the trigger
SELECT COUNT(*) FROM SAMPLE;
```

The SELECT statement returns 1.

```sql
UPDATE TARGET SET A = 2, B = 2; -- does fire the trigger
SELECT COUNT(*) FROM SAMPLE;
```

The SELECT statement returns 2.

### Trigger with an AFTER INSERT and FOR loop

```sql
CREATE ROW TABLE TARGET ( A INT);
 CREATE ROW TABLE control_tab(id INT PRIMARY KEY, name VARCHAR(30), payment
INT);
 CREATE ROW TABLE message_box(message VARCHAR(200), log_time
TIMESTAMP);
 CREATE TRIGGER TEST_TRIGGER_FOR_INSERT
 AFTER INSERT ON TARGET
 BEGIN
     DECLARE v_id        INT := 0;
     DECLARE v_name      VARCHAR(20) := '';
     DECLARE v_pay       INT := 0;
     DECLARE v_msg       VARCHAR(200) := '';
     DELETE FROM message_box;
     FOR v_id IN 100 .. 103 DO
         SELECT name, payment INTO v_name, v_pay FROM control_tab WHERE id
= :v_id;
         v_msg := :v_name || ' has ' || TO_VARCHAR(:v_pay);
         INSERT INTO message_box VALUES (:v_msg, CURRENT_TIMESTAMP);
     END FOR;
 END;
```

### Trigger with EXIT HANDLER examples

```sql
CREATE ROW TABLE TARGET ( A INT);
 CREATE ROW TABLE MYTAB (I INTEGER PRIMARY KEY);

 CREATE TRIGGER MYTRIG_SQLEXCEPTION
 AFTER INSERT ON TARGET
 BEGIN
     DECLARE EXIT HANDLER FOR SQLEXCEPTION RESIGNAL;
     INSERT INTO MYTAB VALUES (1);
     INSERT INTO MYTAB VALUES (1);  -- expected unique violation error: 301
     -- not reached
 END;

 CREATE TRIGGER MYTRIG_SQL_ERROR_CODE
 AFTER UPDATE ON TARGET
 BEGIN
     DECLARE EXIT HANDLER FOR SQL_ERROR_CODE 301 RESIGNAL;
     INSERT INTO MYTAB VALUES (1);
     INSERT INTO MYTAB VALUES (1);  -- expected unique violation error: 301
     -- not reached
 END;

 CREATE TRIGGER MYTRIG_CONDITION
 AFTER DELETE ON TARGET
 BEGIN
     DECLARE MYCOND CONDITION FOR SQL_ERROR_CODE 301;
     DECLARE EXIT HANDLER FOR MYCOND RESIGNAL;
     INSERT INTO MYTAB VALUES (1);
     INSERT INTO MYTAB VALUES (1);  -- expected unique violation error: 301
     -- not reached
 END;
```

### Trigger with SIGNAL/RESIGNAL examples

```sql
CREATE ROW TABLE TARGET ( A INT);
 CREATE ROW TABLE MYTAB (I INTEGER PRIMARY KEY);
 CREATE ROW TABLE MYTAB_TRIGGER_ERR (err_code INTEGER, err_msg VARCHAR(30));
 CREATE TRIGGER MYTRIG_SIGNAL
 AFTER INSERT ON TARGET
 BEGIN
     DECLARE MYCOND CONDITION FOR SQL_ERROR_CODE 10001;
     DECLARE EXIT HANDLER FOR MYCOND INSERT INTO MYTAB_TRIGGER_ERR VALUES
(::SQL_ERROR_CODE, ::SQL_ERROR_MESSAGE);
     INSERT INTO MYTAB VALUES (1);
     SIGNAL MYCOND SET MESSAGE_TEXT = 'my error message1';  -- signal immediately
     -- not reached
     INSERT INTO MYTAB VALUES (2);
 END;
 INSERT INTO SUBJECT VALUES (1)
 SELECT * FROM MYTAB_TRIGGER_ERR;
 (10001, my error message1)

 SELECT * FROM MYTAB;
```

The SELECT statement returns 1.

```sql
CREATE TRIGGER MYTRIG_RESIGNAL
 AFTER UPDATE ON TARGET
 BEGIN
     DECLARE MYCOND CONDITION FOR SQL_ERROR_CODE 10002;
     DECLARE EXIT HANDLER FOR MYCOND RESIGNAL;  -- 2. throws error with error
code 10002
     INSERT INTO MYTAB VALUES (1);
     SIGNAL MYCOND SET MESSAGE_TEXT = 'my error message2';  -- 1. signal
immediately
     -- not reached
     INSERT INTO MYTAB VALUES (2);
 END;
 UPDATE SUBJECT SET A = 100 WHERE A = 1;
 ERR-10002
 ERR-MSG:user-defined error: "TRIGGER_EXCEPTION"."MYTRIG_RESIGNAL": line 4 col
37 (at pos 210): [10002] (range 3) user-defined error exception: my error
message2
```

### Row-wise trigger using transition variable

```sql
CREATE ROW TABLE TARGET ( A INT, B VARCHAR(10));
 CREATE ROW TABLE SAMPLE_OLD ( A INT, B VARCHAR(10));
 CREATE ROW TABLE SAMPLE_NEW ( A INT, B VARCHAR(10));
 CREATE ROW TABLE SAMPLE ( A INT, B VARCHAR(10));
 INSERT INTO TARGET VALUES ( 1, 'oldvalue');
 INSERT INTO TARGET VALUES ( 2, 'oldvalue');
 INSERT INTO TARGET VALUES ( 5, 'oldvalue');
 CREATE TRIGGER TEST_TRIGGER_VAR_UPDATE
 AFTER UPDATE ON TARGET
 REFERENCING NEW ROW mynewrow, OLD ROW myoldrow
 FOR EACH ROW
 BEGIN
  INSERT INTO SAMPLE_new VALUES(:mynewrow.a, :mynewrow.b);
  INSERT INTO SAMPLE_old VALUES(:myoldrow.a, :myoldrow.b);
  INSERT INTO SAMPLE VALUES(0, 'trigger');
 END;
 UPDATE TARGET SET b = 'newvalue' WHERE A < 3;
 SELECT * FROM TARGET;
 1, 'newvalue'
 2, 'newvalue'
 5, 'oldvalue'
 SELECT * FROM SAMPLE_NEW;
 1, 'newvalue'
 2, 'newvalue'
 SELECT * FROM SAMPLE_OLD;
 1, 'oldvalue'
 2, 'oldvalue'
 SELECT * FROM SAMPLE;
 0, 'trigger'
 0, 'trigger'
```

### Statement-wise trigger using transition table

```sql
CREATE ROW TABLE TARGET ( A INT, B VARCHAR(10));
 CREATE ROW TABLE SAMPLE_OLD ( A INT, B VARCHAR(10));
 CREATE ROW TABLE SAMPLE_NEW ( A INT, B VARCHAR(10));
 CREATE ROW TABLE SAMPLE ( A INT, B VARCHAR(10));
 INSERT INTO TARGET VALUES ( 1, 'oldvalue');
 INSERT INTO TARGET VALUES ( 2, 'oldvalue');
 INSERT INTO TARGET VALUES ( 5, 'oldvalue');
 CREATE TRIGGER TEST_TRIGGER_TAB_UPDATE
 AFTER UPDATE ON TARGET
 REFERENCING NEW TABLE mynewtab, OLD TABLE myoldtab
 FOR EACH STATEMENT
 BEGIN
  INSERT INTO SAMPLE_new SELECT * FROM :mynewtab;
  INSERT INTO SAMPLE_old SELECT * FROM :myoldtab;
  INSERT INTO SAMPLE VALUES(0, 'trigger');
 END;
 UPDATE TARGET SET b = 'newvalue' WHERE A < 3;
 SELECT * FROM TARGET;
 1, 'newvalue'
 2, 'newvalue'
 5, 'oldvalue'
 SELECT * FROM SAMPLE_NEW;
 1, 'newvalue'
 2, 'newvalue'
 SELECT * FROM SAMPLE_OLD;
 1, 'oldvalue'
 2, 'oldvalue'
 SELECT * FROM SAMPLE;
 0, 'trigger'
CREATE ROW TABLE T1(A INTEGER PRIMARY KEY, B INTEGER);
CREATE COLUMN TABLE T2(A INTEGER PRIMARY KEY, C INTEGER);
CREATE VIEW V1 AS (SELECT T1.A A, B, C, T1.A+10 D FROM T1, T2 WHERE T1.A = T2.A);
CREATE TRIGGER TR1 INSTEAD OF INSERT ON V1 REFERENCING NEW ROW NEW
BEGIN
    INSERT INTO T1 VALUES(:NEW.A, :NEW.B);
    INSERT INTO T2 VALUES(:NEW.A, :NEW.C);
END;
INSERT INTO V1(A,B,C) VALUES(1,2,3);
SELECT FROM T1 ORDER BY A, B;
```

The SELECT statement returns 1, 2.

```sql
SELECT FROM T2 ORDER BY A, C;
```

The SELECT statement returns 1, 3.

```sql
SELECT FROM V1 ORDER BY A, B, C, D;
```

The SELECT statement returns 1, 2, 3, 11

```sql
CREATE TRIGGER TR2 INSTEAD OF UPDATE ON V1 REFERENCING OLD ROW OLD, NEW ROW NEW
BEGIN
    UPDATE T1 SET A=:NEW.A, B=:NEW.B WHERE A=:OLD.A;
    UPDATE T2 SET A=:NEW.A, C=:NEW.C WHERE A=:OLD.A;
END;
UPDATE V1 SET A = 5, B = 6, C = 7 WHERE A = 1;
SELECT FROM T1 ORDER BY A, B;
```

The SELECT statement returns 5, 6.

```sql
SELECT FROM T2 ORDER BY A, C;
```

The SELECT statement returns 5, 7.

```sql
SELECT FROM V1 ORDER BY A, B, C, D;
```

The SELECT statement returns 5, 6, 7, 11.

```sql
CREATE TRIGGER TR3 INSTEAD OF DELETE ON V1 REFERENCING OLD ROW OLD
BEGIN
    DELETE FROM T1 WHERE A = :OLD.A;
    DELETE FROM T2 WHERE A = :OLD.A;
END;
DELETE FROM V1;
SELECT FROM T1 ORDER BY A, B;
SELECT FROM T2 ORDER BY A, C;
SELECT FROM V1 ORDER BY A, B, C, D;
```

## Related Information

TRIGGERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/TRIGGERS-System-View.md) Introduction to SQL [→](../../4.01-Introduction-to-SQL.md) Data Types [→](../../4.03-Data-Types/README.md) Expressions [→](../../4.06-Expressions.md) CREATE PROCEDURE Statement (Procedural) [→](CREATE-PROCEDURE-Statement-Procedural.md) Predicates [→](../../4.07-Predicates/README.md) INSERT Statement (Data Manipulation) [→](INSERT-Statement-Data-Manipulation.md) DELETE Statement (Data Manipulation) [→](DELETE-Statement-Data-Manipulation.md) UPDATE Statement (Data Manipulation) [→](UPDATE-Statement-Data-Manipulation.md) REPLACE Statement (Data Manipulation) [→](REPLACE-Statement-Data-Manipulation.md) SELECT Statement (Data Manipulation) [→](4.10.01.144-SELECT/README.md) TRIGGERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/TRIGGERS-System-View.md)
