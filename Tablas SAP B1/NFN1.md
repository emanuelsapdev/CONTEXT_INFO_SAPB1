# NFN1 - Not a Fiscal Sequence

- **Tabla:** NFN1
- **Descripción:** Not a Fiscal Sequence
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/NFN1.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | [ONFN](ONFN.md) |  |  |
| 2 | `SeqCode` | Seq. Code | Int | 6 | - | 0 |  |
| 3 | `SeqName` | Seq. Name | nVarChar | 8 | - |  |  |
| 4 | `InitialNum` | Initial Number | Int | 11 | - | 0 |  |
| 5 | `NextNum` | Next Number for Use | Int | 11 | - | 0 |  |
| 6 | `LastNum` | Last Number Allowed | Int | 11 | - |  |  |
| 7 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 8 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 9 | `Remark` | Remarks | nVarChar | 50 | - |  |  |
| 10 | `GroupCode` | Group | Int | 6 | - | 1 | `1`<br>`2`<br>`3`<br>`4`<br>`5`<br>`6`<br>`7`<br>`8`<br>`9`<br>`10` |
| 11 | `Locked` | Locked | VarChar | 1 | - | N | `Y`<br>`N` |
| 12 | `YearTransf` | Year-End Closing | VarChar | 1 | - | N | `Y`<br>`N` |
| 13 | `Indicator` | Period Indicator | nVarChar | 10 | [OPID](OPID.md) | ' ' | `' '` |
| 14 | `Template` | Template | nVarChar | 20 | - |  |  |
| 15 | `NumSize` | Numeric Size | Int | 11 | - |  |  |
| 16 | `Prefix` | Prefix | nVarChar | 8 | - |  |  |
| 17 | `Suffix` | Suffix | nVarChar | 8 | - |  |  |
| 18 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- |  |
| 19 | `Model` | Nota Fiscal Model | nVarChar | 6 | [ONFM](ONFM.md) | 0 |  |
| 20 | `Location` | Location Code | Int | 11 | [OLCT](OLCT.md) |  |  |
| 21 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) | 0 |  |
| 22 | `IsDigital` | Digital Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `EnvTypeNFe` | Environment Type NF-e | Int | 11 | [OBNI](OBNI.md) | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, DocSubType, SeqCode |
| S_NAME | Yes | ObjectCode, DocSubType, BPLId, SeqName |
