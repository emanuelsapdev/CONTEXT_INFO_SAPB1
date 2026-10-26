# CAEA - CAEA Information

- **Tabla:** CAEA
- **Descripción:** CAEA Information
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CAEA.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Regime` | Regime | VarChar | 1 | - |  |  |
| 2 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 3 | `Period` | CAEA Period | Int | 11 | - |  |  |
| 4 | `Orden` | CAEA Order | Int | 11 | - |  |  |
| 5 | `Status` | CAEA Status | VarChar | 1 | - | N | `N` = New Created<br>`S` = Request Sent<br>`E` = Error Received<br>`U` = Not Used<br>`T` = Reporting Pending<br>`P` = Partially Reported<br>`F` = Fully Reported |
| 6 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| PERIOD | No | Regime, Period, Orden |
