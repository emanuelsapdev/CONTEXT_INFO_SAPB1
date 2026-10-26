# CTBR - Toolbars

- **Tabla:** CTBR
- **Descripción:** Toolbars
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CTBR.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserSign` |  | Int | 6 | [OUSR](OUSR.md) |  |  |
| 2 | `ToolbarId` |  | Int | 11 | - |  |  |
| 3 | `Docking` |  | Int | 6 | - |  |  |
| 4 | `LeftID` |  | Int | 6 | - |  |  |
| 5 | `TopID` |  | Int | 6 | - |  |  |
| 6 | `RightID` |  | Int | 6 | - |  |  |
| 7 | `BottomID` |  | Int | 6 | - |  |  |
| 8 | `VisibleID` |  | VarChar | 1 | - | N | `Y`<br>`N` |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserSign, ToolbarId |
