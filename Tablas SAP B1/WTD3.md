# WTD3 - WTax Codes Details for BP

- **Tabla:** WTD3
- **Descripción:** WTax Codes Details for BP
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTD3.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OWTD](OWTD.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `WTCode` | WTax Code | nVarChar | 4 | - |  |  |
| 4 | `KeyPart1` | BP Key Part 1 | nVarChar | 15 | - |  |  |
| 5 | `KeyPart2` | BP Key Part 2 | nVarChar | 15 | - |  |  |
| 6 | `DateFrom` | Effective Date From | Date | 8 | - |  |  |
| 7 | `DateTo` | Effective Date To | Date | 8 | - |  |  |
| 8 | `Rate` | Currency Rate | Num | 19.6 | - |  |  |
| 9 | `DetailType` | Type of Detailed Information | nVarChar | 2 | - |  | `A` = Allowed<br>`S` = Special Rate<br>`E` = Exemption |
| 10 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`P` = Partner Implementation<br>`U` = UI Reproweb Autocomplete |
| 11 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
| BP | Yes | WTCode, KeyPart1, KeyPart2, DateFrom, DetailType |
