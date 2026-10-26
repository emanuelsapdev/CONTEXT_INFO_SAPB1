# ODRP - Personal Data Retention Periods

- **Tabla:** ODRP
- **Descripción:** Personal Data Retention Periods
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODRP.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PeriodCode` | Period Code | nVarChar | 20 | - |  |  |
| 3 | `PeriodName` | Period Description | nVarChar | 100 | - |  |  |
| 4 | `DatSubType` | Data Subject Type | nVarChar | 4 | - |  | `OCRD` = Business Partner<br>`OCPR` = Contact Person<br>`OHEM` = Employee<br>`OUSR` = User<br>`CPN1` = Campaign - BP<br>`OUDO` = User-Defined Object |
| 5 | `ObjType` | Object Type | Int | 11 | - | -1 | `-1` = All<br>`2` = Business Partner<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery Notes<br>`234000031` = Return Request<br>`16` = Return<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Return Request<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`69` = Landed Costs<br>`24` = Incoming Payments<br>`46` = Outgoing Payments<br>`57` = Checks for Payment |
| 6 | `PeriodYear` | Period Years | Int | 11 | - |  |  |
| 7 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Active<br>`N` = Inactive |
| 8 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 9 | `CreateTime` | Creation Time | Int | 11 | - |  |  |
| 10 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 11 | `UpdateTime` | Update Time | Int | 11 | - |  |  |
| 12 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 14 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 15 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 16 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | PeriodCode |
