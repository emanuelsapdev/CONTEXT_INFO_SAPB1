# ANS1 - Customer Equipment Card - Multiple Business Partners - History

- **Tabla:** ANS1
- **Descripción:** Customer Equipment Card - Multiple Business Partners - History
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ANS1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `InsID` | Equipment Card No. | Int | 11 | [OINS](OINS.md) |  |  |
| 2 | `BpCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | InsID, BpCode, LogInstanc |
