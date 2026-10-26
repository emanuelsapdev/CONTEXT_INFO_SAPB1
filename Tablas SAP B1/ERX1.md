# ERX1 - Excise Registering Number-Rows

- **Tabla:** ERX1
- **Descripción:** Excise Registering Number-Rows
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ERX1.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ErnId` | Excise Register Numbering ID | Int | 11 | [OERX](OERX.md) |  |  |
| 2 | `NumTypeId` | Numbering Type ID | Int | 11 | - |  |  |
| 3 | `NumTypeNam` | Numbering Type Name | nVarChar | 30 | - |  |  |
| 4 | `FirstNum` | First Number | Int | 11 | - |  |  |
| 5 | `NextNum` | Next Number | Int | 11 | - |  |  |
| 6 | `LastNum` | Last Number | Int | 11 | - |  |  |
| 7 | `ResetDate` | Date of last reset | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ErnId, NumTypeId |
