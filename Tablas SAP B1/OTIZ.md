# OTIZ - Company Time Zone

- **Tabla:** OTIZ
- **Descripción:** Company Time Zone
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTIZ.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Id` | Index | Int | 11 | - |  |  |
| 2 | `ChangeDate` | Date of Change | nVarChar | 50 | - |  |  |
| 3 | `TimeZone` | Index of Time Zone | Int | 11 | - |  |  |
| 4 | `ActiveDst` | Indicator: DST Active or Not | VarChar | 1 | - | U | `Y`<br>`N`<br>`U` |
| 5 | `offset` | Offset | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Id |
