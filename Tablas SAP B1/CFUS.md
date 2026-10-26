# CFUS - Functionality Usage Statistics

- **Tabla:** CFUS
- **Descripción:** Functionality Usage Statistics
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CFUS.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FuncName` | Function Name | nVarChar | 100 | - |  |  |
| 2 | `UserCode` | User Code | nVarChar | 25 | - |  |  |
| 3 | `Count` | Total No. of Records | Int | 11 | - |  |  |
| 4 | `Since` | Since Date | Date | 8 | - |  |  |
| 5 | `LastUse` | Last Use Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FuncName, UserCode |
