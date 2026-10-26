# OBSL - Warehouse Sublevel

- **Tabla:** OBSL
- **Descripción:** Warehouse Sublevel
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBSL.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `FldAbs` | Bin Field Conf. Internal Number | Int | 11 | [OBFC](OBFC.md) |  |  |
| 3 | `SLCode` | Code | nVarChar | 50 | - |  |  |
| 4 | `Descr` | Description | nVarChar | 50 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N |  |
| 8 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 13 | `Deleted` | Deleted | VarChar | 1 | - | N |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| BUSINESS_K | Yes | FldAbs, SLCode |
