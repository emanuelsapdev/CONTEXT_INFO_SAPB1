# 4.10.1.6 ALTER FULLTEXT INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 428–431

Changes the parameters of a fulltext index or the state of an index processing queue.

## Syntax

```sql
ALTER FULLTEXT INDEX <index_name> <alter_fulltext_index_option>
```

## Syntax Elements

#### index_name

Specifies the name of the fulltext index to be rebuilt with an optional schema name.

```sql
<index_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### alter_fulltext_index_option

Specifies whether the parameters of the fulltext index or the state of the fulltext index queue should be changed.

```sql
<alter_fulltext_index_option> ::=
 <fulltext_parameter_list>
| <queue_command> QUEUE
```

Specifying `<queue_command>` QUEUE is only possible for an asynchronous explicit fulltext index.

##### fulltext_parameter_list

Specifies a list of fulltext index parameters that are to be changed.

```sql
<fulltext_parameter_list> ::=
 <fulltext_parameter> [, <fulltext_parameter> [,…] ]
```

##### fulltext_parameter

Specifies fulltext index parameters.

```sql
<fulltext_parameter> ::=
 FUZZY SEARCH INDEX <on_off>
 | PHRASE INDEX RATIO <index_ratio>
 | TEXT MINING <on_off>
 | TEXT MINING CONFIGURATION <string>
 | TEXT MINING CONFIGURATION OVERLAY <string>
```

##### FUZZY SEARCH INDEX on_off

Defines if a fuzzy search index is used.

```sql
FUZZY SEARCH INDEX <on_off>
<on_off> ::= { ON | OFF }
```

ON switches on the fuzzy search index, and OFF turns the fuzzy search index off.

##### PHRASE INDEX RATIO index_ratio

Specifies the phrase index ratio.

```sql
PHRASE INDEX RATIO <index_ratio>
```

##### index_ratio

Specifies the percentage of the phrase index ratio.

```sql
<index_ratio> ::= <exact_numeric_literal>
```

The value used must be between 0.0 and 1.0

##### queue_command

Specifies an action to be performed on the index queue.

```sql
<queue_command> ::=
  FLUSH
 | SUSPEND
 | ACTIVATE
```

##### FLUSH

Updates the fulltext index with the documents in the queue that have already been processed.

##### SUSPEND

Suspends the fulltext index processing queue.

##### ACTIVATE

Activates the fulltext index processing queue.

##### TEXT MINING on_off

Enables/disables text mining on the indexed column.

```sql
TEXT MINING <on_off>
```

Text mining initialization will be called when the fulltext index is created.

##### TEXT MINING CONFIGURATION string

Specifies the text mining configuration name to use.

```sql
TEXT MINING CONFIGURATION <string>
```

Also invokes text mining initialization.

##### TEXT MINING CONFIGURATION OVERLAY string

Specifies certain text mining parameters to override the text mining configuration.

```sql
TEXT MINING CONFIGURATION OVERLAY <string>
```

Also invokes text mining initialization.

## Description

The queue is a mechanism used to enable a fulltext index to operate in asynchronous manner; that is, inserts do not block until a document is processed.

## Examples

Create table T and then add two indexes i1 and i2. Index i1 is a synchronous fulltext index, i2 is an asynchronous fulltext index.

```sql
CREATE COLUMN TABLE T (c1 NVARCHAR(1000), c2 NVARCHAR(1000));
 CREATE FULLTEXT INDEX i1 ON T (c1) SYNC;
 CREATE FULLTEXT INDEX i2 ON T (c2) ASYNC;
```

Alter the phrase index to 30 percent and turn on the fuzzy search index for indexes i1 and i2.

```sql
ALTER FULLTEXT INDEX i1 PHRASE INDEX RATIO 0.3 FUZZY SEARCH INDEX ON;
 ALTER FULLTEXT INDEX i2 PHRASE INDEX RATIO 0.3 FUZZY SEARCH INDEX ON;
```

Suspend the queue for fulltext index i2.

```sql
ALTER FULLTEXT INDEX i2 SUSPEND QUEUE;
```

Update the fulltext index with the documents in the queue that have already been processed.

```sql
ALTER FULLTEXT INDEX i2 FLUSH QUEUE;
```
