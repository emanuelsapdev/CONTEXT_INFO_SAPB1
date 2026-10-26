# NFN4 - Manual Nota Fiscal Number

- **Tabla:** NFN4
- **Descripción:** Manual Nota Fiscal Number
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NFN4.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | [ONFN](ONFN.md) |  |  |
| 2 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 3 | `SeqName` | Seq Name | nVarChar | 8 | - |  |  |
| 4 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 5 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 6 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 7 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |
| 8 | `Model` | Nota Fiscal Model | nVarChar | 6 | [ONFM](ONFM.md) |  |  |
| 9 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) | - |  |
| 10 | `DocEntry` | Document Abs. Entry | Int | 11 | - |  |  |
| 11 | `DocNumber` | Document Number | Int | 11 | - |  |  |
| 12 | `IsReusable` | Is Reusable | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, Serial, SeriesStr, SubStr, Model, SeqCode, CardCode |
