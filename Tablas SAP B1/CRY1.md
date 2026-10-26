# CRY1 - Country Combination Settings

- **Tabla:** CRY1
- **Descripción:** Country Combination Settings
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CRY1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Country` | Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 2 | `TransCRY` | Transaction Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 3 | `EnableIST` | Enable Intrastat Transactions | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Country, TransCRY |
