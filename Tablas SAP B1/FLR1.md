# FLR1 - Filter Lines

- **Tabla:** FLR1
- **Descripción:** Filter Lines
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/FLR1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsId` | Foreign Key | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `ColName` | Column Name | nVarChar | 10 | - |  |  |
| 4 | `CompValue` | Compare Value | nVarChar | 254 | - |  |  |
| 5 | `CompOper` | Compare Operator | nVarChar | 2 | - | = | `=` = =<br>`>` = ><br>`<</td>` = <</td><br>`>=` = >=<br>`<=` = <=<br>`!=` = != |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsId, ColName |
