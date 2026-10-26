# CPRC - Contact Persons - Communication Mean

- **Tabla:** CPRC
- **Descripción:** Contact Persons - Communication Mean
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CPRC.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CntctCode` | Internal Number | Int | 11 | [OCPR](OCPR.md) |  |  |
| 2 | `CommMeanID` | Communication Mean ID | Int | 11 | [OCMM](OCMM.md) |  |  |
| 3 | `Select` | Select | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 4 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 5 | `CntctName` | Contact Person Name | nVarChar | 50 | [OCPR](OCPR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CntctCode, CommMeanID |
