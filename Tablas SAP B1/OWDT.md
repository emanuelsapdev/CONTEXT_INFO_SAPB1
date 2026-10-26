# OWDT - Widget Table

- **Tabla:** OWDT
- **Descripción:** Widget Table
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OWDT.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Widget Name | nVarChar | 20 | - |  |  |
| 3 | `UserSign` | User ID | nVarChar | 6 | [OUSR](OUSR.md) |  |  |
| 4 | `Prototype` | Prototype | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
