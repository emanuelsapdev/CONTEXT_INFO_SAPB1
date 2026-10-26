# OPR4 - Opportunity - Interests

- **Tabla:** OPR4
- **Descripción:** Opportunity - Interests
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPR4.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OprId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Line` | Row No. | Int | 6 | - |  |  |
| 3 | `IntId` | Interest ID | Int | 11 | [OOIN](OOIN.md) |  |  |
| 4 | `Prmry` | Primary Interest | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OprId, Line |
