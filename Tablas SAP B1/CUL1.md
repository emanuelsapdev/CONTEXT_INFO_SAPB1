# CUL1 - Customer Usage Statistics Log

- **Tabla:** CUL1
- **Descripción:** Customer Usage Statistics Log
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUL1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ParrentDoc` | Parent Document | Int | 11 | - |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `Param` | Parameter | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ParrentDoc, LineNum |
