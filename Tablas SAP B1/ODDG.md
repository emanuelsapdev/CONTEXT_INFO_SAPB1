# ODDG - Withholding Tax Deduction Groups

- **Tabla:** ODDG
- **Descripción:** Withholding Tax Deduction Groups
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODDG.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Numerator` | Group Key | Int | 11 | - |  |  |
| 2 | `DdgCode` | Group Code | nVarChar | 2 | [ODGL](ODGL.md) |  |  |
| 3 | `DdgName` | Group Name | nVarChar | 30 | - |  |  |
| 4 | `DdctPrcnt` | Max. Red. in % | Num | 19.6 | - |  |  |
| 5 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Numerator |
| NAME | Yes | DdgCode, DdgName |
