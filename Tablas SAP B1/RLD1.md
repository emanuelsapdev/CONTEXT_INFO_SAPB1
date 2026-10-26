# RLD1 - Reference Links Definition

- **Tabla:** RLD1
- **Descripción:** Reference Links Definition
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RLD1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ORLD](ORLD.md) |  |  |
| 2 | `TargetType` | Target Type | VarChar | 1 | - | H | `H` = Header<br>`B` = BP Row<br>`L` = Row |
| 3 | `TargetFld` | Target Field | nVarChar | 50 | - |  |  |
| 4 | `SourceFld` | Source Field | nVarChar | 50 | - |  |  |
| 5 | `OrderNum` | Order Number | Int | 11 | - |  |  |
| 6 | `SourceType` | Source Type | VarChar | 1 | - | E | `B` = Base Document Reference<br>`C` = Column<br>`D` = Default<br>`E` = Not Defined<br>`I` = Installment Number<br>`S` = Reference Link Sources<br>`T` = Remarks Template |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, TargetType, TargetFld |
