# AST1 - Sales Tax Codes - Rows

- **Tabla:** AST1
- **Descripción:** Sales Tax Codes - Rows
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AST1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `STCCode` | STC Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 2 | `Line_ID` | Row Number | Int | 11 | - | 0 |  |
| 3 | `STACode` | STA Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 4 | `STAType` | STA Type | Int | 11 | [OSTA](OSTA.md) |  |  |
| 5 | `TaxOnTCode` | STA Tax on Tax Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 6 | `TaxOnTType` | STA Tax On Tax Type | Int | 11 | [OSTA](OSTA.md) |  |  |
| 7 | `EfctivRate` | Effective Rate | Num | 19.6 | - |  |  |
| 8 | `FmlId` | Tax Formula ID | Int | 11 | [OFML](OFML.md) |  |  |
| 9 | `CstCodeIn` | CST Code Incoming | nVarChar | 20 | - |  |  |
| 10 | `CstSuffix` | CST Suffix for ICMS | nVarChar | 2 | - |  |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | STCCode, Line_ID, LogInstanc |
