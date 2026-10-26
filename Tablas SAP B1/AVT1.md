# AVT1 - Tax Definition

- **Tabla:** AVT1
- **Descripción:** Tax Definition
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AVT1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Group Code | nVarChar | 8 | - |  |  |
| 2 | `EffecDate` | Effective from | Date | 8 | - |  |  |
| 3 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 4 | `EquVatPr` | Equalization Tax % | Num | 19.6 | - |  |  |
| 5 | `MinAmount` | Minimum Stamp Tax Amount | Num | 19.6 | - |  |  |
| 6 | `FixedAmout` | Fixed Stamp Tax Amount | Num | 19.6 | - |  |  |
| 7 | `TaxType` | Tax Type (VAT or Stamp) | VarChar | 1 | - | V | `V` = VAT<br>`S` = Stamp |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `DatevCode` | DATEV Code | Int | 6 | - |  |  |
| 10 | `DTV13BCode` | Datev Transactions Deliveries and Services | nVarChar | 50 | [ODTS](ODTS.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, EffecDate, LogInstanc |
