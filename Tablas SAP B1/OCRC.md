# OCRC - Credit Cards

- **Tabla:** OCRC
- **Descripción:** Credit Cards
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCRC.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CreditCard` | Credit Card Code | Int | 6 | - |  |  |
| 2 | `CardName` | Credit Card Name | nVarChar | 30 | - |  |  |
| 3 | `AcctCode` | G/L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 4 | `Phone` | Telephone | nVarChar | 50 | - |  |  |
| 5 | `CompanyId` | Company ID | nVarChar | 20 | - |  |  |
| 6 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 11 | `IntTaxCode` | Internal Tax Code | nVarChar | 2 | - |  | `1` = Isracard<br>`2` = CAL<br>`3` = Diners<br>`4` = American Express<br>`6` = Leumi Card |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `Country` | Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CreditCard |
| CARD_NAME | Yes | CardName |
