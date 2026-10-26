# OPR2 - Opportunity - Partners

- **Tabla:** OPR2
- **Descripción:** Opportunity - Partners
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPR2.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OpportId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Line` | Row No. | Int | 6 | - |  |  |
| 3 | `ParterId` | Partners | Int | 11 | [OPRT](OPRT.md) |  |  |
| 4 | `Memo` | Details | nVarChar | 50 | - |  |  |
| 5 | `OrlCode` | Relationship Code | Int | 11 | [OORL](OORL.md) |  |  |
| 6 | `RelatCard` | Related BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 7 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OpportId, Line |
