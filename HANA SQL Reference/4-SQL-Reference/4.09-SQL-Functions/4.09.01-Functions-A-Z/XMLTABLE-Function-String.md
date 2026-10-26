# 4.9.1.236 XMLTABLE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 392–398

Creates a relational table from an XML string.

## Syntax

```sql
XMLTABLE( [ <XML_namespace_clause>, ]
 <row_pattern> PASSING <XML_argument> COLUMNS <column_definitions>
 <error_option>
)
```

## Syntax Elements

#### XML_namespace_clause

Defines the XML namespace.

```sql
XMLNAMESPACE (<XML_namespace>[, ...]
 [DEFAULT <default_namespace>]
)
```

##### XML_namespace

Specifies the XML namespace.

```sql
<XML_namespace> ::= <namespace_url> AS <namespace_alias>
```

When the XMLNAMESPACE clause is specified, the result contains only the records that belong to the specified namespaces. If the namespace URL is specified (DEFAULT `<namespace_url>`), then all XPath strings should refer to the namespace URL.

##### default_namespace

Specifies the default namespace. `<default_namespace>`, `<namespace_url>`, and `<namespace_alias>` are string constants.

#### row_pattern

Describes the format of the xmlNodes in the XML with an XPath expression.

```sql
<row_pattern> ::= <str_const>
```

#### XML_argument

Specifies the XML to be converted to a table, defined as either as a string constant or a column reference.

```sql
<XML_argument> ::=
 <str_const>
 | <column_ref>
```

##### str_const

Specifies an XML string to be converted to a table.

##### column_ref

Specifies a column containing the XML to be converted to a table.

#### column_definitions

Defines the columns in the result table.

```sql
<column_definitions> ::=
 <column_name> <column_type> [, <column_name> <column_type>,...]
```

##### column_name

Specifies the column name.

```sql
<column_name> ::= <identifier>
```

##### column_type

Specifies a data type for the column.

```sql
<column_type> ::=
 FOR ORDINALITY
 | <regular_column_return_type> PATH <column_pattern> [DEFAULT <str_const>]
 | <formatted_column_return_type> FORMAT XML PATH <column_pattern>
[DEFAULT <str_const>]
```

If the column is an ordinality column, then the value for the I-th row is I. The return type of the ordinality column is BIGINT.

If the column is a regular column, then the value for the I-th row can be defined as follows:

- If the result value is not empty, then the result comes from applying `<row_pattern>` or `<column_pattern>` to `<XML_argument>`.
- If the result value is empty, then the result comes from the default value of `<column_definition>`.
- If no default value is specified, then NULL is returned.
- If FORMAT XML is specified, then the result contains the XML tags and XML structure instead of returning the value.

##### regular_column_return_type

Specifies the return type of the column.

```sql
<regular_column_return_type> ::=
BIGINT
 | DATE
 | DECIMAL
 | DOUBLE
 | INT
 | NVARCHAR (<int_const>)
 | SECONDDATE
 | SMALLDECIMAL
 | TIME
 | TIMESTAMP
 | VARCHAR (<int_const>)
```

##### column_pattern

Specifies the xPath Expression to use to extract the value for a column.

```sql
<column_pattern> ::= <str_const>
```

##### formatted_column_return_type

Specifies the list of possible return types for the formatted column in the resulting table.

```sql
<formatted_column_return_type> ::= VARCHAR (<int_const>)
 | NVARCHAR (<int_const>)
```

#### error_option

Returns an exception when an error occurs during table creation.

```sql
<error_option> ::= ERROR ON ERROR
```

If ERROR ON ERROR is not set, then an empty result is returned. If ERROR ON ERROR is specified, then a runtime error is returned instead of a DEFAULT or an empty result.

## Description

Use the XMLTABLE function as a replacement for the FROM clause in a query to extract the data from an XML string. The XMLTABLE function returns the data as a relational table.

ERROR ON ERROR explicitly returns an error on a runtime error, since the default behavior is to return NULL in cases of a runtime error.

FORMAT XML extracts a result in XML format.

The resulting table has a row for each element in the XML string, which is the result of applying the `<row_pattern>` to the `<XML_argument>`. The rows of the resulting table have a column for each `<column_definition>`, with the `<column_name>` and `<return_type>` specified.

You cannot call the XMLTABLE function in the FROM clause of an UPDATE or DELETE statement.

## Example

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE('/doc/item' PASSING
'<doc>
  <item><id>10</id><name>Box</name></item>
  <item><id>20</id><name>Jar</name></item>
</doc>'
COLUMNS
ID INT PATH 'id',
NAME VARCHAR(20) PATH 'name'
) as XTABLE;
```

| **ID** | **NAME** |
| --- | --- |
| 10 | Box |
| 20 | Jar |

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE('/doc/item' PASSING
'<doc>
  <item><id>10</id><name>Box</name></item>
  <item><id>20</id><name>Jar</name></item>
</doc>'
COLUMNS
RN FOR ORDINALITY,
NAME VARCHAR(20) PATH 'name'
) as XTABLE;
```

| **RN** | **NAME** |
| --- | --- |
| 1 | Box |
| 2 | Jar |

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE('/doc/item' PASSING
'<doc>
  <item><id>10</id><name>Box</name></item>
  <item><id>20</id><name>Jar</name></item>
</doc>'
COLUMNS
ID NVARCHAR(20) FORMAT XML PATH 'id',
NAME VARCHAR(20) FORMAT XML PATH 'name'
) AS XTABLE;
```

| **ID** | **NAME** |
| --- | --- |
| \<id>10\</id> | \<name>Box\</name> |
| \<id>20\</id> | \<name>Jar\</name> |

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE('/doc/item' PASSING
'<doc>
  <item><id subid="one">10</id><name>Box</name></item>
  <item><id subid="two">20</id><name>Jar</name></item>
</doc>'
COLUMNS
ID NVARCHAR(20) PATH 'id/@subid',
NAME VARCHAR(20) PATH 'name'
) AS XTABLE;
```

| **ID** | **NAME** |
| --- | --- |
| one | Box |
| two | Jar |

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE(
XMLNAMESPACE('http://www.sap.com/xmltable' AS 'sap'),
'/sap:doc/sap:item' PASSING
'<sap:doc xmlns:sap="http://www.sap.com/xmltable">
  <sap:item><sap:id>1</sap:id><sap:name>Box</sap:name></sap:item>
  <sap:item><sap:id>2</sap:id><sap:name>Jar</sap:name></sap:item>
</sap:doc>'
COLUMNS
ID INT PATH 'sap:id',
NAME VARCHAR(20) PATH 'sap:name'
) as XTABLE;
```

| **ID** | **NAME** |
| --- | --- |
| 1 | Box |
| 2 | Jar |

The following example returns the table below:

```sql
CREATE ROW TABLE XMLDATA (XML VARCHAR(5000));
INSERT INTO XMLDATA VALUES (
'<sap:doc xmlns:sap="http://www.sap.com/xmltable">
  <sap:item><sap:id>1</sap:id><sap:name>Box</sap:name></sap:item>
  <sap:item><sap:id>2</sap:id><sap:name>Jar</sap:name></sap:item>
</sap:doc>');
INSERT INTO XMLDATA VALUES (
'<labs:doc xmlns:labs="http://www.saplabskorea.com/xmltable">
  <labs:item><labs:id>1</labs:id><labs:name>Apple</labs:name></labs:item>
  <labs:item><labs:id>2</labs:id><labs:name>Coconut</labs:name></labs:item>
</labs:doc>');
SELECT * FROM
XMLTABLE(XMLNAMESPACE('http://www.saplabskorea.com/xmltable' AS 'myns'),
'/myns:doc/myns:item' PASSING
XMLDATA.XML
COLUMNS
ID INT PATH 'myns:id',
NAME VARCHAR(20) PATH 'myns:name'
) AS XTABLE;
```

| **ID** | **NAME** |
| --- | --- |
| 1 | Apple |
| 2 | Coconut |

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE(XMLNAMESPACE('http://www.sap.com/xmltable' AS 'myns', 'http://
www.namespace.com/name' as 'myns2'),
  '/myns:doc/myns:item' PASSING
  '<sap:doc xmlns:sap= "http://www.sap.com/xmltable" xmlns:ns2= "http://
www.namespace.com/name">
 <sap:item><sap:id>1</sap:id><sap:name>Box</sap:name><ns2:count>3</ns2:count></
sap:item>
 <sap:item><sap:id>2</sap:id><sap:name>Jar</sap:name><ns2:count>4</ns2:count></
sap:item>
 </sap:doc>'
 COLUMNS
  ID INT PATH 'myns:id',
  NAME VARCHAR(20) PATH 'myns:name',
  COUNT INT PATH 'myns2:count'
) AS XTABLE;
```

| **ID** | **NAME** | **COUNT** |
| --- | --- | --- |
| 1 | Box | 3 |
| 2 | Jar | 4 |

The following example returns the table below:

```sql
SELECT * FROM
XMLTABLE(
XMLNAMESPACE('http://www.namespace.com/name' AS 'myns2' DEFAULT 'http://
www.sap.com/xmltable'),
'/doc/item' PASSING
'<sap:doc xmlns:sap="http://www.sap.com/xmltable" xmlns:ns="http://
www.namespace.com/name">
  <sap:item><sap:id>1</sap:id><ns:name>Box</ns:name></sap:item>
  <sap:item><sap:id>2</sap:id><ns:name>Jar</ns:name></sap:item>
</sap:doc>'
COLUMNS
ID INT PATH 'id',
NAME VARCHAR(20) PATH 'myns2:name'
) AS XTABLE;
```

| **ID** | **NAME** |
| --- | --- |
| 1 | Box |
| 2 | Jar |
