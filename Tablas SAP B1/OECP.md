# OECP - Expense Classification Type

- **Tabla:** OECP
- **Descripción:** Expense Classification Type
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OECP.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Unique Entry | Int | 11 | - |  |  |
| 2 | `Code` | Code | nVarChar | 50 | - |  |  |
| 3 | `Descriptio` | Description | nVarChar | 254 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE | Yes | Code |
