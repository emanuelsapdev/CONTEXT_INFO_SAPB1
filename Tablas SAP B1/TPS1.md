# TPS1 - Tax Parameter Attributes

- **Tabla:** TPS1
- **Descripción:** Tax Parameter Attributes
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TPS1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TpsId` | Tax Parameter Set | Int | 11 | [OTPS](OTPS.md) |  |  |
| 2 | `DispOrder` | Display Order | Int | 11 | - |  |  |
| 3 | `TpaId` | ID of Attributes Mapping | Int | 11 | [OTPA](OTPA.md) |  |  |
| 4 | `Mandatory` | Mandatory to Input | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TpsId, TpaId |
| ORDER | Yes | TpsId, DispOrder |
