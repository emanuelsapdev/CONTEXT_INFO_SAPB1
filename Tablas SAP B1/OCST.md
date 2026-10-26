# OCST - States

- **Tabla:** OCST
- **Descripción:** States
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCST.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 3 | - |  |  |
| 2 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 3 | `Name` | Name | nVarChar | 100 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `eCode` | eCode | Int | 6 | - |  |  |
| 6 | `GNRECode` | GNRE Code | nVarChar | 4 | - |  |  |
| 7 | `GSTCode` | GST State Code | nVarChar | 2 | - |  |  |
| 8 | `GSTIsUT` | Is Union Territory | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `GroupCode` | Group Code | Int | 6 | [OSTG](OSTG.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Country, Code |
| GST_CODE | No | GSTCode, Country |
