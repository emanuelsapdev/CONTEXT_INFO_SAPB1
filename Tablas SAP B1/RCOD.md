# RCOD - RCOD

- **Tabla:** RCOD
- **Descripción:** RCOD
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RCOD.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Base Doc Code | nVarChar | 8 | - |  |  |
| 2 | `TrnsDocCod` | Translation Doc Code | nVarChar | 8 | - |  |  |
| 3 | `ClntDocCod` | Client Doc Code | nVarChar | 8 | - |  |  |
| 4 | `LocMask` | Localization Mask | nVarChar | 100 | - |  |  |
| 5 | `LangMask` | Language Mask | nVarChar | 100 | - |  |  |
| 6 | `TranRequir` | Translation Required | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocCode |
