# XAP2 - XAPP Widget

- **Tabla:** XAP2
- **Descripción:** XAPP Widget
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XAP2.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Key of widget | Int | 11 | - |  |  |
| 2 | `PageEntry` | Foreign of XAPP page | Int | 11 | - |  |  |
| 3 | `Type` | Widget Type | nVarChar | 250 | - |  |  |
| 4 | `ObjEntry` | Foeign key of widget content | Int | 11 | - |  |  |
| 5 | `Width` | Width of widget | Int | 11 | - |  |  |
| 6 | `Height` | Height of widget | Int | 11 | - |  |  |
| 7 | `Index` | Order of widget | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
