# FAA1 - Asset Attributes - Rows

- **Tabla:** FAA1
- **Descripción:** Asset Attributes - Rows
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FAA1.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | [OFAA](OFAA.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `AttrID` | Attribute ID | Int | 11 | - |  |  |
| 4 | `AttrName` | Attribute Name | nVarChar | 100 | - |  |  |
| 5 | `FieldType` | Field Type | VarChar | 1 | - |  | `A` = Text<br>`N` = Numeric<br>`D` = Date<br>`S` = Amount<br>`P` = Price<br>`Q` = Quantity |
| 6 | `DefaultVal` | Default Value | nVarChar | 100 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `SnapshotId` | Snapshot ID | Int | 11 | - | 0 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineNum |
| UNIQUE | Yes | Code, AttrID |
