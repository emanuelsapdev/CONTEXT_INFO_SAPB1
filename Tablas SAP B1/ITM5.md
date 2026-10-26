# ITM5 - Asset Item Projects

- **Tabla:** ITM5
- **Descripción:** Asset Item Projects
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITM5.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ValidFrom` | Valid From | Date | 8 | - |  |  |
| 4 | `ValidTo` | Valid To | Date | 8 | - |  |  |
| 5 | `Project` | Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 6 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 7 | `ObjType` | Object | nVarChar | 20 | [ADP1](ADP1.md) | 4 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, LineNum |
