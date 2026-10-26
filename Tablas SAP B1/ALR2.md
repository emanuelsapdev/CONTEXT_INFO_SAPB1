# ALR2 - Dynamic message data row

- **Tabla:** ALR2
- **Descripción:** Dynamic message data row
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ALR2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Internal Number | Int | 11 | [OALR](OALR.md) |  |  |
| 2 | `Location` | The order of columns in message | Int | 11 | - |  |  |
| 3 | `ColName` | The column name in message | nVarChar | 30 | - |  |  |
| 4 | `Link` | Link Indication | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Location |
