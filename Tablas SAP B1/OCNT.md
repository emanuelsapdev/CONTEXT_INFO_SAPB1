# OCNT - Counties

- **Tabla:** OCNT
- **Descripción:** Counties
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCNT.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Auto Key | Int | 11 | - |  |  |
| 2 | `Code` | County Code | nVarChar | 7 | - |  |  |
| 3 | `Country` | Country/Region | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 4 | `State` | State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 5 | `Name` | County Name | nVarChar | 100 | - |  |  |
| 6 | `TaxZone` | Tax Free Zone | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `IbgeCode` | IBGE Code | nVarChar | 10 | - |  |  |
| 8 | `GiaCode` | GIA Code | nVarChar | 10 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| UNIQUE | Yes | Code, Country, State |
