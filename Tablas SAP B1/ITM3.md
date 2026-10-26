# ITM3 - Items - Localization Fields

- **Tabla:** ITM3
- **Descripción:** Items - Localization Fields
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM3.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `IncNature` | Income Nature | nVarChar | 10 | [OBMI](OBMI.md) |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 4 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode |
