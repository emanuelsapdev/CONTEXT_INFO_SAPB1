# OERT - Excise Register Numbering Type

- **Tabla:** OERT
- **Descripción:** Excise Register Numbering Type
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OERT.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `NumTypeId` | Numbering Type ID | Int | 11 | - |  |  |
| 2 | `NumTypeNam` | Numbering Type Name | nVarChar | 30 | - |  |  |
| 3 | `FirstNum` | First Number | Int | 11 | - |  |  |
| 4 | `NextNum` | Next Number | Int | 11 | - |  |  |
| 5 | `LastNum` | Last Number | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | NumTypeId |
| TYPE_NAME | Yes | NumTypeNam |
