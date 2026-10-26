# RCI1 - Recipient List - Rows

- **Tabla:** RCI1
- **Descripción:** Recipient List - Rows
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RCI1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | [ORCI](ORCI.md) |  |  |
| 2 | `LineNum` | Addressee Number | Int | 11 | - |  |  |
| 3 | `ObjType` | Object | nVarChar | 20 | - |  | `12` = User<br>`171` = Employee |
| 4 | `ObjCode` | Object Code | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LineNum |
