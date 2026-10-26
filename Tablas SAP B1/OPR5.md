# OPR5 - Opportunity - Reasons

- **Tabla:** OPR5
- **Descripción:** Opportunity - Reasons
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPR5.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OpportId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Line` | Row No. | Int | 6 | - |  |  |
| 3 | `ReasondId` | Reason | Int | 11 | [OOFR](OOFR.md) |  |  |
| 4 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OpportId, Line |
