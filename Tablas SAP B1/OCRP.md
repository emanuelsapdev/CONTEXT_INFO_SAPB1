# OCRP - Payment Methods

- **Tabla:** OCRP
- **Descripción:** Payment Methods
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRP.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CrTypeCode` | Payment Method Code | Int | 6 | - |  |  |
| 2 | `CrTypeName` | Name | nVarChar | 30 | - |  |  |
| 3 | `CreditCard` | Assigned to Credit Card | Int | 6 | [OCRC](OCRC.md) |  |  |
| 4 | `DueTerms` | Payment Code | nVarChar | 8 | [OCDT](OCDT.md) |  |  |
| 5 | `MinCredit` | Minimum Credit Amount | Num | 19.6 | - |  |  |
| 6 | `MinToPay` | Minimum Payment Amount | Num | 19.6 | - |  |  |
| 7 | `MaxValid` | Max. Qty Without Approval | Num | 19.6 | - |  |  |
| 8 | `InstalMent` | Installment Payments Possible | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No<br>`C` = Cr<br>`L` = Rd |
| 9 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 11 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CrTypeCode |
| NAME | Yes | CrTypeName |
| CRED_CODE | No | CreditCard |
| INSTALMENT | No | InstalMent |
