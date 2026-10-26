# OBOT - Bill Of Exchang Transaction

- **Tabla:** OBOT
- **Descripción:** Bill Of Exchang Transaction
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBOT.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | BOE Transaction key | Int | 11 | - |  |  |
| 2 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 3 | `StatusFrom` | Status from | VarChar | 1 | - |  | `S` = Sent<br>`G` = Generated<br>`D` = Deposit<br>`P` = Paid<br>`F` = Failed<br>`V` = BoE to Vendor |
| 4 | `StatusTo` | Status To | VarChar | 1 | - |  | `C` = Canceled<br>`G` = Generated<br>`D` = Deposit<br>`P` = Paid<br>`F` = Failed<br>`L` = Closed<br>`V` = BoE to Vendor |
| 5 | `TranDate` | Transaction Date | Date | 8 | - |  |  |
| 6 | `TranTime` | Transaction Time | Int | 6 | - |  |  |
| 7 | `Reconciled` | was the Boe Reconciled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 9 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 10 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 11 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 12 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
