# 4.10.1.19.38 ALTER SYSTEM RECLAIM DATAVOLUME Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 528–529

Frees unused space inside an SAP HANA database disk persistence.

## Syntax

```sql
ALTER SYSTEM RECLAIM DATAVOLUME [SPACE] [<host_port>]
   <percentage_of_payload_size> <shrink_mode>
```

## Syntax Elements

#### host_port

Specifies the server on which the size of the persistence should be reduced.

```sql
<host_port> ::= '<hostname>:<port_number>'
```

If `<host_port>` is omitted, then the statement is distributed to all servers with the persistence.

For information about hostname and port number, see notation_host_name_and_port "Notation".

#### percentage_of_overload_size

Specifies the desired percentage of the payload to which the data volume should be reduced.

```sql
<percentage_of_overload_size> ::= <unsigned_integer>
```

The value must not be smaller than 105. The recommended values are between 105 and 120.

#### shrink_mode

Specifies the strategy to be used to reduce the persistence size. Currently only defragment is supported.

```sql
<shrink_mode> ::= DEFRAGMENT
```

## Description

This statement reduces data volume size to a percentage of payload size. This statement works in a similar way to defragmenting a hard drive. Pages that are scattered around a data volume are moved to the front of the volume, and the free space at the end of the data volume is truncated.

## Example

The following statement defragments the persistence of all servers in the landscape and reduces them to 120% of the payload size.

```sql
ALTER SYSTEM RECLAIM DATAVOLUME 120 DEFRAGMENT;
```
