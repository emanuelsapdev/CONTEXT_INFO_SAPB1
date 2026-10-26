# 4.10.1.49 CREATE FULLTEXT INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 708–711

Creates an explicit fulltext index on the specified table column.

## Syntax

```sql
CREATE FULLTEXT INDEX <index_name> ON <table_name> ( <column_name> )
   [ <fulltext_parameter_list> ]
```

## Syntax Elements

#### index_name

Specifies the name of the fulltext index to be created, with optional schema name.

```sql
<index_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### fulltext_parameter_list

Specifies the fulltext parameters.

```sql
<fulltext_parameter_list> ::= <fulltext_parameter> [, <fulltext_parameter> [,
…] ]
<fulltext_parameter> ::=
 LANGUAGE COLUMN <column_name>
 | LANGUAGE DETECTION ( <string_literal_list> )
 | MIME TYPE COLUMN <column_name>
 | <change_tracking_elem>
 | FUZZY SEARCH INDEX  { ON | OFF }
 | PHRASE INDEX RATIO <index_ratio>
 | CONFIGURATION <string_literal>
 | SEARCH ONLY  { ON | OFF }
 | FAST PREPROCESS  { ON | OFF }
 | TEXT ANALYSIS  { ON | OFF }
 | MIME TYPE <string_literal>
 | TOKEN SEPARATORS <string_literal>
 | TEXT MINING { ON | OFF }
 | TEXT MINING CONFIGURATION <string_literal>
 | TEXT MINING CONFIGURATION OVERLAY <string_literal>
<column_name> ::= <identifier>
```

##### LANGUAGE COLUMN column_name

Defines the column where the language of a document is specified.

##### LANGUAGE DETECTION ( string_literal_list )

Specifies the set of languages to be considered during language detection.

##### MIME TYPE COLUMN column_name

Defines the column where the mime-type of a document is specified.

##### change_tracking_elem

Specifies the type of index to be created.

```sql
<change_tracking_elem> ::=
 SYNC[HRONOUS]
 | ASYNC[HRONOUS] [FLUSH [QUEUE] <flush_queue_elem>]
```

###### SYNC[HRONOUS]

Creates a synchronous fulltext index.

###### ASYNC[HRONOUS]

Creates an asynchronous fulltext index.

###### flush_queue_elem

Specifies when to update the fulltext index if an asynchronous index is used.

```sql
FLUSH [QUEUE] <flush_queue_elem>
<flush_queue_elem> ::=
 EVERY <integer_literal> MINUTES
 | AFTER <integer_literal> DOCUMENTS
 | EVERY <integer_literal> MINUTES OR AFTER <integer_literal> DOCUMENTS
```

When DOCUMENTS is specified, the fulltext index is updated after the specified number of changes to the table, including updates and deletes.

##### FUZZY SEARCH INDEX { ON | OFF }

Specifies whether a fuzzy search index should be used.

##### PHRASE INDEX RATIO index_ratio

Specifies the percentage of the phrase index. Value must be between 0.0 and 1.0

```sql
PHRASE INDEX RATIO <index_ratio>
<index_ratio> ::= <exact_numeric_literal>
```

##### CONFIGURATION string_literal

Specifies the name of a standard text analysis configuration, or the fullyqualified name of a custom text analysis configuration stored in the HANA Repository, created with the HANA Deployment Infrastructure, or created with the TEXT_CONFIGURATION_CREATE stored procedure.

If the configuration was created with HANA DI, then the HANA DI container must be the same as the schema for the fulltext index. If the configuration was created with TEXT_CONFIGURATION_CREATE, then the configuration must have been created with the same schema name as the schema for the fulltext index.

##### SEARCH ONLY { ON | OFF }

Controls whether the original document should be stored (OFF) or only the search relevant tokens. If set to ON, then unsearchable parts of the document are removed.

##### FAST PREPROCESS { ON | OFF }

Controls whether fast preprocessing is used. If set to ON, then fast preprocessing is used and linguistic searches are not possible.

##### TEXT ANALYSIS { ON | OFF }

Enables text analysis capabilities on the indexed column. Text analysis can extract entities such as persons, products, or places from documents, which are stored in a new table.

##### MIME TYPE string_literal

Specifies the default mime type used for preprocessing. The value must be a valid mime type. For example, 'cf M_TEXT_ANALYSIS_MIME_TYPES'.

##### TOKEN SEPARATORS string_literal

Specifies a set of characters used for token separation. Only ASCII characters are considered.

##### TEXT MINING { ON | OFF }

Controls whether to enable text mining. If set to ON, then text mining capabilities will be initialized on the indexed column when the fulltext index is created. Text mining provides functionality that can compare documents by examining the terms used within them.

##### TEXT MINING CONFIGURATION string_literal

Specifies the name of a standard text mining configuration, or the fullyqualified name of a custom text mining configuration stored in the HANA Repository, created with the HANA Deployment Infrastructure, or created with the TEXT_CONFIGURATION_CREATE stored procedure. If the configuration was created with HANA DI, then the HANA DI container must be the same as the schema for the fulltext index. If the configuration was created with TEXT_CONFIGURATION_CREATE, then the configuration must have been created with the same schema name as the schema for the fulltext index.

##### TEXT MINING CONFIGURATION OVERLAY string_literal

Specifies literal text mining configuration data that should override the text mining configuration file. The format is the same as in the configuration file, typically a small subset of parameters. This allows parameter experimentation without requiring creation of configuration files for each case.

## Description

A fulltext index is supported for the following data types:

- VARCHAR, NVARCHAR types with CS_STRING type
- VARBINARY type
- BLOB, CLOB, NCLOB types

## Example

Create table A.

```sql
CREATE COLUMN TABLE A (A VARCHAR(10) PRIMARY KEY, B VARCHAR(10));
```

Create a synchronous fulltext index named i. Index i is on column A of table A, where the fuzzy search index is not used and the set of languages for language detection consists of EN, DE, and KR.

```sql
CREATE FULLTEXT INDEX i ON A(A) FUZZY SEARCH INDEX OFF
   SYNC LANGUAGE DETECTION ('EN','DE','KR');
```
