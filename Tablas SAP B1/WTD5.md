# WTD5 - WTax Codes Details for Freight

- **Tabla:** WTD5
- **Descripción:** WTax Codes Details for Freight
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTD5.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OWTD](OWTD.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `WTCode` | WTax Code | nVarChar | 4 | - |  |  |
| 4 | `ExpnsCode` | Freight Code | Int | 11 | [OEXD](OEXD.md) |  |  |
| 5 | `DateFrom` | Effective Date From | Date | 8 | - |  |  |
| 6 | `DateTo` | Effective Date To | Date | 8 | - |  |  |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`P` = Partner Implementation |
| 8 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
| EXPNSCODE | Yes | WTCode, ExpnsCode, DateFrom |
