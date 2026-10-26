# XAP4 - Widget Item

- **Tabla:** XAP4
- **Descripción:** Widget Item
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/XAP4.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Key of filter item | Int | 11 | - |  |  |
| 2 | `FilEntry` | Foreign key of filter | Int | 11 | - |  |  |
| 3 | `TarEntry` | Target content Entry | Int | 11 | - |  |  |
| 4 | `TarType` | Target content type | nVarChar | 250 | - |  |  |
| 5 | `TarField` | Target field | nVarChar | 250 | - |  |  |
| 6 | `IsBase` | Is base or not | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
