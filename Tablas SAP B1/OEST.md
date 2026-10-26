# OEST - EWB Sub-Type

- **Tabla:** OEST
- **Descripción:** EWB Sub-Type
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEST.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `SubID` | EWB Sub-Type Code | Int | 11 | - |  |  |
| 3 | `SubType` | Sub supply type of e-way bill | nVarChar | 50 | - |  |  |
| 4 | `SuplyType` | EWB Supply Type | VarChar | 1 | - | B | `B` = Both<br>`I` = Inward<br>`O` = Outward |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SUB_TYPE | Yes | SubID |
| SUPLY_TYPE | No | SuplyType |
