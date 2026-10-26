# 4.9.1.121 MAP Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 247–248

Searches for an expression within a set of values and returns a specified result.

## Syntax

```sql
MAP(<expression>, <search_value>, <result> [, <search_value>, <result> [...] ]
[, <default_result>])
```

## Syntax Elements

#### expression

Specifies the expression to search for in any of the `<search>` values.

#### search_value

Specifies a value to search for `<expression>` in. You can specify more than one search value, and for each `<search_value>` value you can specify a corresponding `<result>`.

#### result

Specifies the result to return when `<expression>` is found in the corresponding `<search_value>` value.

#### default_result

Specifies the default result to return when `<expression>` is not found in any of the `<search_value>` values.

## Description

Searches for `<expression>` within a set of search values and returns the corresponding result.

- If `<expression>` is not found and `<default_result>` is defined, then MAP returns `<default_result>`.
- If `<expression>` is not found and `<default_result>` is not defined, then MAP returns NULL.

`<search_value>` and corresponding `<result>` values must be specified as pairs.

## Example

The following query searches for 2, finds it in the third `<search>`/`<result>` pair (`2, 'Two'`), and returns the configured `<result>` value `Two`.

```sql
SELECT MAP(2, 0, 'Zero', 1, 'One', 2, 'Two', 3, 'Three', 'Default') "map" FROM
DUMMY;
```

The following searches for 99 in the `<search>` values, and, not finding it, returns the `<default_result>` value `Default`.

```sql
SELECT MAP(99, 0, 'Zero', 1, 'One', 2, 'Two', 3, 'Three', 'Default') "map" FROM
DUMMY;
```

The following searches for 99 in the `<search>` values, and, not finding it, returns NULL because no `<default_result>` was specified.

```sql
SELECT MAP(99, 0, 'Zero', 1, 'One', 2, 'Two', 3, 'Three') "map" FROM DUMMY;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
