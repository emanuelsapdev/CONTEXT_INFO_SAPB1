# TCD3 - Tax Code Determination

- **Tabla:** TCD3
- **Descripción:** Tax Code Determination
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TCD3.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Internal Number | Int | 11 | - |  |  |
| 2 | `Tcd2Id` | Determination Key Field ID | Int | 11 | [TCD2](TCD2.md) |  |  |
| 3 | `EfctFrom` | Effective From | Date | 8 | - |  |  |
| 4 | `EfctTo` | Effective To | Date | 8 | - |  |  |
| 5 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 6 | `TcdId` | Tax Determination Code | Int | 11 | [OTCD](OTCD.md) |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId |
| TCD3_UNI | Yes | Tcd2Id, EfctFrom |
