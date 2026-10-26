# OEUT - EWB Unit

- **Tabla:** OEUT
- **Descripción:** EWB Unit
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEUT.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `UnitCode` | EWB Unit Code | nVarChar | 3 | - |  |  |
| 3 | `UnitName` | EWB Unit Name | nVarChar | 30 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| UNIT_CODE | Yes | UnitCode |
