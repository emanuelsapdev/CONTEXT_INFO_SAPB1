# OPRT - Partners

- **Tabla:** OPRT
- **Descripción:** Partners
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPRT.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrtId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 15 | - |  |  |
| 3 | `RelatnType` | Relationship Type | nVarChar | 20 | - |  |  |
| 4 | `RelatCard` | Related BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 5 | `Memo` | Details | nVarChar | 50 | - |  |  |
| 6 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `DefaultORL` | Relationship | Int | 11 | [OORL](OORL.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrtId |
| NAME | Yes | Name |
