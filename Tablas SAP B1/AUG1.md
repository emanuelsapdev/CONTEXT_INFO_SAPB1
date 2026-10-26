# AUG1 - UoM Group Detail

- **Tabla:** AUG1
- **Descripción:** UoM Group Detail
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AUG1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UgpEntry` | UoM Group Abs. Entry | Int | 11 | [OUGP](OUGP.md) |  |  |
| 2 | `UomEntry` | UoM Abs. Entry | Int | 11 | [OUOM](OUOM.md) |  |  |
| 3 | `AltQty` | Alternative Quantity | Num | 19.6 | - |  |  |
| 4 | `BaseQty` | Base Quantity | Num | 19.6 | - |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 6 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 7 | `WghtFactor` | Weight Factor | Int | 6 | [OWGT](OWGT.md) | 0 |  |
| 8 | `UdfFactor` | UDF Factor | Int | 11 | - | -1 |  |
| 9 | `IsActive` | Is Active or Not | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `BaseUdfFtr` | Base UDF Factor | Int | 11 | - | -1 |  |
| 11 | `BaseWgtFtr` | Base Weight Factor | Int | 6 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UgpEntry, LineNum, LogInstanc |
