# UDO1 - User-Defined Objects - Child

- **Tabla:** UDO1
- **Descripción:** User-Defined Objects - Child
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UDO1.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 20 | - |  |  |
| 2 | `SonNum` | Child No. | Int | 11 | - |  |  |
| 3 | `TableName` | Table Name | nVarChar | 19 | [OUTB](OUTB.md) |  |  |
| 4 | `LogName` | Log Table Name | nVarChar | 20 | - |  |  |
| 5 | `SonName` | Child Name | nVarChar | 100 | - | ' ' |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, SonNum |
