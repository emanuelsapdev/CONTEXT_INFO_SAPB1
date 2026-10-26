# DATB - Data Archive Tax Balance

- **Tabla:** DATB
- **Descripción:** Data Archive Tax Balance
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DATB.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Numerator | Int | 11 | - |  |  |
| 2 | `LocCode` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 3 | `NfTaxId` | ID of Nota Fiscal Tax Category | Int | 11 | [ONFT](ONFT.md) |  |  |
| 4 | `TaxComId` | Tax Component ID | Int | 11 | [OSTT](OSTT.md) |  |  |
| 5 | `MatType` | Material Type | Int | 11 | - |  |  |
| 6 | `ArchBal` | Data Archived Balance | Num | 19.6 | - |  |  |
| 7 | `TaxAcct` | Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `IsPLA` | PLA Field | VarChar | 1 | - |  |  |
| 9 | `IsTaxCred` | Tax Credit Field | VarChar | 1 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
