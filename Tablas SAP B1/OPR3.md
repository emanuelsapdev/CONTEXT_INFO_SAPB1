# OPR3 - Opportunity - Competitors

- **Tabla:** OPR3
- **Descripción:** Opportunity - Competitors
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPR3.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `OpportId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Line` | Row No. | Int | 6 | - |  |  |
| 3 | `CompetId` | Competitors | Int | 11 | [OCMT](OCMT.md) |  |  |
| 4 | `Memo` | Details | nVarChar | 50 | - |  |  |
| 5 | `Won` | Won or Lost | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `ThreatLevl` | Threat Level | Int | 6 | - |  | `1` = Low<br>`2` = Medium<br>`3` = High |
| 7 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | OpportId, Line |
