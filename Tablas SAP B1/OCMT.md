# OCMT - Competitors

- **Tabla:** OCMT
- **Descripción:** Competitors
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCMT.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CompetId` | Sequence No. | Int | 11 | - |  |  |
| 2 | `Name` | Name | nVarChar | 15 | - |  |  |
| 3 | `ThreatLevl` | Threat Level | Int | 6 | - | 1 | `1` = Low<br>`2` = Medium<br>`3` = High |
| 4 | `Memo` | Details | nVarChar | 50 | - |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CompetId |
| NAME | Yes | Name |
