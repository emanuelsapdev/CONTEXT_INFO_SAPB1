# TFC1 - Tax Type Combination - Rows

- **Tabla:** TFC1
- **Descripción:** Tax Type Combination - Rows
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TFC1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TfcId` | TFC ID | Int | 11 | [OTFC](OTFC.md) |  |  |
| 2 | `DispOrder` | Display Order | Int | 11 | - |  |  |
| 3 | `TypeId` | Tax Type ID | Int | 11 | [OSTT](OSTT.md) |  |  |
| 4 | `FmlId` | Formula ID | Int | 11 | [OFML](OFML.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TfcId, DispOrder |
| TAXTYPE | No | TypeId |
