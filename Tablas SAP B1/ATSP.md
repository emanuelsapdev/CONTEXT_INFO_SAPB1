# ATSP - Transporters

- **Tabla:** ATSP
- **Descripción:** Transporters
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATSP.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Transporter Abs. Entry | Int | 11 | - |  |  |
| 2 | `TransCode` | Transporter Code | nVarChar | 20 | - |  |  |
| 3 | `TransName` | Transporter Name | nVarChar | 25 | - |  |  |
| 4 | `TransID` | Transporter ID | nVarChar | 15 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 9 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 10 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
