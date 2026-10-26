# ALR3 - Dynamic message data cells

- **Tabla:** ALR3
- **Descripción:** Dynamic message data cells
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ALR3.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Internal Number | Int | 11 | [OALR](OALR.md) |  |  |
| 2 | `Location` | Number of Column in Message | Int | 11 | - |  |  |
| 3 | `Line` | Number of Column in Message | Int | 11 | - |  |  |
| 4 | `Value` | The column/row value | nVarChar | 254 | - |  |  |
| 5 | `ObjType` | The linked object | nVarChar | 20 | - |  |  |
| 6 | `KeyStr` | Key string in linked object | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, Location, Line |
