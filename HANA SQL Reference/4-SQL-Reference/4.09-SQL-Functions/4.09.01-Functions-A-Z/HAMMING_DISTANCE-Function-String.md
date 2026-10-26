# 4.9.1.87 HAMMING_DISTANCE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 196–198

Performs a bitwise or bytewise comparison between two arguments and returns the hamming distance.

## Syntax

```sql
HAMMING_DISTANCE(<left_hand_side>, <right_hand_side>)
```

## Syntax Elements

#### left_hand_side

Specifies a left hand side argument against which `<right_hand_side>` is compared.

```sql
<lhs> ::= <string>
```

#### right_hand_side

Specifies a right hand side argument to compare against `<left_hand_side>`

```sql
<rhs> ::= <string>
```

## Description

Hamming distance describes differences between two specified arguments, and reflects the number of corresponding positions that differ from each other across the two arguments. Integer and binary arguments are compared bitwise, whereas string arguments are compared byte-wise.

The HAMMING_DISTANCE function returns -1 if the length of the two arguments is different, and NULL if either of the arguments is NULL.

## Examples

The following example returns `-1` because the arguments are of different length:

```sql
SELECT HAMMING_DISTANCE('abc', 'ca') "hamming_distance" FROM DUMMY;
```

The following example returns `0` because the arguments are identical:

```sql
SELECT HAMMING_DISTANCE('abc', 'abc') "hamming_distance" FROM DUMMY;
```

The following example returns `0` because the arguments are identical:

```sql
SELECT HAMMING_DISTANCE(4, 4) "hamming_distance" FROM DUMMY;
```

The following example returns `3` because all positions in the two arguments are different from the other string:

```sql
SELECT HAMMING_DISTANCE('abc', 'cab') "hamming_distance" FROM DUMMY;
```

The following example returns `4` to reflect the bitwise comparison of the arguments:

```sql
SELECT HAMMING_DISTANCE(TO_BINARY('abc'), TO_BINARY('cab')) "hamming_distance"
FROM DUMMY;
```

The following example returns `3` to reflect the bitwise comparison of the arguments:

```sql
SELECT HAMMING_DISTANCE(4, 9) "hamming_distance" FROM DUMMY;
```

The following example returns `-1` because the binary arguments are of different length:

```sql
SELECT HAMMING_DISTANCE(to_binary('abc'), to_binary('ca')) "hamming_distance"
FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
