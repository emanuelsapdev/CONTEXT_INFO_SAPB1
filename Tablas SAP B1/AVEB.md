# AVEB - VAT Exemptions for Business Partners - History

- **Tabla:** AVEB
- **Descripción:** VAT Exemptions for Business Partners - History
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AVEB.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 11 | `Comments` | Remarks | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
| BP_CODE | Yes | CardCode, LogInstanc |
