# ALR1 - Queue of messages to be sent

- **Tabla:** ALR1
- **Descripción:** Queue of messages to be sent
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ALR1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Internal Number | Int | 11 | [OALR](OALR.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `NameFrom` | From | nVarChar | 155 | - |  |  |
| 4 | `AddrFrom` | Reply Address | nVarChar | 100 | - |  |  |
| 5 | `NameTo` | To | nVarChar | 155 | - |  |  |
| 6 | `IsSMS` | SMS | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`F` = Fax<br>`O` = MS365 |
| 7 | `Address` | Address | nVarChar | 100 | - |  |  |
| 8 | `Status` | Status | VarChar | 1 | - | U | `U` = Not Sent<br>`P` = In Process<br>`S` = Sent |
| 9 | `ObjType` | Object | nVarChar | 20 | - |  |  |
| 10 | `ObjCode` | Object Code | nVarChar | 50 | - |  |  |
| 11 | `SendAs` | Send As | VarChar | 1 | - | 0 | `0` = To<br>`1` = Cc<br>`2` = Bcc |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineId |
| STATUS | No | Status |
