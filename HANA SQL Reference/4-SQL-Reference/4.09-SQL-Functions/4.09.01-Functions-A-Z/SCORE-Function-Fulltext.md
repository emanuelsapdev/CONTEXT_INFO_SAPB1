# 4.9.1.165 SCORE Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 303–305

Returns the relevance of a record that has been found.

## Syntax

```sql
SCORE()
```

## Description

For search queries using the CONTAINS predicate, use SCORE to obtain the relevance of a record that has been found. SCORE returns a real value between 0 and 1. The SAP HANA database calculates a score based on the following information:

- The relevance, or weighting, of attributes in a search using the CONTAINS predicate. The relevance of a match depends on the weight of the column that caused the match. You can specify weights as you create the view, or in the CONTAINS predicate.
- Fuzziness in a fuzzy search. The more exact matching that occurs, the higher the score is.
- Text ranking (TF-IDF).

## Examples

The following example creates a table that contains two strings:

```sql
CREATE COLUMN TABLE T (CONTENT TEXT FAST PREPROCESS OFF);
 INSERT INTO T VALUES('This is a test.');
 INSERT INTO T VALUES('This was a test.');
```

Use the SCORE function to check the table contents for relevance against the search string 'is':

```sql
SELECT SCORE(), CONTENT FROM T WHERE CONTAINS(CONTENT, 'is', LINGUISTIC);
```

| **SCORE** | **CONTENT** |
| --- | --- |
| 0.8700000047683716 | This is a test. |
| 0.40833336114883423 | This was a test. |

The following example creates a fictitious table that contains two strings:

```sql
CREATE COLUMN TABLE T (CONTENT TEXT FAST PREPROCESS OFF);
 INSERT INTO T VALUES('example');
 INSERT INTO T VALUES('example');
```

Use the SCORE function to check the table contents for similarity to the string 'example':

```sql
SELECT SCORE(), CONTENT FROM T WHERE CONTAINS(CONTENT, 'example',Fuzzy(0.8));
```

| **SCORE** | **CONTENT** |
| --- | --- |
| 1 | example |
| 1 | example |

## Related Information

[CONTAINS Predicate](../../4.07-Predicates/4.07.03-CONTAINS-Predicate.md)
