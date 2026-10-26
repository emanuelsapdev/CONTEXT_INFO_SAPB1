# OALI - Alternative Items 2

- **Tabla:** OALI
- **Descripción:** Alternative Items 2
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OALI.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OrigItem` | Original Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `AltItem` | Alternative Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `Match` | Match Factor | Num | 19.6 | - |  |  |
| 4 | `Remarks` | Item Remarks | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OrigItem, AltItem |
