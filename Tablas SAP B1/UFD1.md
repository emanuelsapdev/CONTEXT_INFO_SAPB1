# UFD1 - User Fields - Values Definitions

- **Tabla:** UFD1
- **Descripción:** User Fields - Values Definitions
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UFD1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TableID` | Table | nVarChar | 21 | - |  |  |
| 2 | `FieldID` | Field | Int | 6 | - |  |  |
| 3 | `IndexID` | Index | Int | 6 | - |  |  |
| 4 | `FldValue` | Value | nVarChar | 254 | - |  |  |
| 5 | `Descr` | Description | nVarChar | 254 | - |  |  |
| 6 | `FldDate` | Date Value | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TableID, FieldID, IndexID |
