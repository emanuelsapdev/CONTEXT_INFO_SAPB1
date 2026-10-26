# ORCN - Retail Chains

- **Tabla:** ORCN
- **Descripción:** Retail Chains
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORCN.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ChainCode` | Internal Number | Int | 11 | - |  |  |
| 2 | `ChainName` | Chain Name | nVarChar | 20 | - |  |  |
| 3 | `SuppNum` | Vendor Code | nVarChar | 20 | - |  |  |
| 4 | `SuppName` | Vendor Name | nVarChar | 20 | - |  |  |
| 5 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `SavePath` | File Path | Text | 16 | - |  |  |
| 7 | `UsePartSup` | Use Goods Del. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `BaseCode` | Basic Grid Template | Int | 11 | - | -1 |  |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `ExportNum` | Export Counter | Int | 11 | - | 0 |  |
| 11 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ChainCode |
| NAME | Yes | ChainName |
