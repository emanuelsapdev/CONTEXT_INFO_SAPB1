# OWTD - Withholding Tax Definition

- **Tabla:** OWTD
- **Descripción:** Withholding Tax Definition
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWTD.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `WTCode` | WTax Code | nVarChar | 4 | - |  |  |
| 3 | `WTName` | WTax Code Name | nVarChar | 50 | - |  |  |
| 4 | `Rate` | Rate | Num | 19.6 | - |  |  |
| 5 | `EffecDate` | Effective From | Date | 8 | - |  |  |
| 6 | `Inactive` | Inactive | VarChar | 1 | - | N | `Y`<br>`N` |
| 7 | `OffclCode` | Official Code | nVarChar | 15 | - |  |  |
| 8 | `Category` | Category | VarChar | 1 | - | P | `I` = Invoice<br>`P` = Payment |
| 9 | `BaseType` | Base Type | VarChar | 1 | - | N | `N` = Net<br>`V` = VAT<br>`G` = Gross<br>`H` = Gross - VAT |
| 10 | `WTTypeId` | Type | Int | 11 | [OWTT](OWTT.md) |  |  |
| 11 | `BaseMin` | Min. Amount | Num | 19.6 | - |  |  |
| 12 | `PrctBsAmnt` | % Base Amount | Num | 19.6 | - |  |  |
| 13 | `FmlId` | Formula ID | Int | 11 | [OFML](OFML.md) |  |  |
| 14 | `Account` | Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `SlScProgr` | Sliding Scale Progressive Tax | VarChar | 1 | - | N | `Y`<br>`N` |
| 16 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 17 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 18 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 19 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 20 | `CalcWHTCrM` | Calculate Withholding Tax in Automatic Credit Memo | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| WT_CODE | Yes | WTCode |
| WT_NAME | No | WTName |
