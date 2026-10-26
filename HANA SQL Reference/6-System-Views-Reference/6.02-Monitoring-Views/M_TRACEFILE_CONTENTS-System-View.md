# 6.2.336 M_TRACEFILE_CONTENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2113–2114

Provides SAP HANA information from trace files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| FILE_NAME | VARCHAR(256) | Displays the file name. |
| OFFSET | BIGINT | Displays the file offset in bytes. |
| CONTENT | NVARCHAR(1000) | Displays the file content at the offset. |

## Additional Information

This view requires an equal predicate on HOST and FILE_NAME as part of the WHERE clause. Use HOST, FILE_NAME as returned by the view M_TRACEFILES to prevent unintentional materialization of all trace files.

The optional WHERE clause `OFFSET<,<=,=,>,>= value` is efficiently handled by this view. With `OFFSET > -value`, you can read from the end of the file without having to know the file size in advance. With `OFFSET <> -value`, you can read from the start and end of a file. Do not use the equivalent `OFFSET < value OR OFFSET >-value` because this is very inefficient for large files and returns duplicates for small files where the file size is < 2\*value.

Trace files typically contain ASCII or CESU-8, but they can also contain binary data. To support all types of data, each byte from the trace file is encoded as one NVARCHAR with values in the range 0 to 255. To recode as CESU-8 you have to use code like in this Python example:

```sql
cursor.execute(" select CONTENT from M_TRACEFILE_CONTENTS where HOST='...' and
FILE_NAME='...' ")
filedata=''
for row in cursor.fetchall():
    filedata += row[1].encode('latin-1') # reinterpret as bytearray
displaydata = filedata.decode('utf-8','replace') # do not use 'strict' error
handling
```

## Related Information

M_TRACEFILES System View [→](M_TRACEFILES-System-View.md) ALTER SYSTEM CLEAR TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-TRACES-Statement-System-Management.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) M_SERVICE_TRACES System View [→](M_SERVICE_TRACES-System-View.md)
