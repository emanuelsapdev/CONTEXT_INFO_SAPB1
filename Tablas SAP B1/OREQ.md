# OREQ - External System Call Request

- **Tabla:** OREQ
- **Descripción:** External System Call Request
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OREQ.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Request ID | Int | 11 | - |  |  |
| 2 | `Category` | Request Category | Int | 11 | - |  |  |
| 3 | `Status` | Request Status | VarChar | 1 | - | N | `N` = New<br>`P` = In Process<br>`S` = Completed<br>`C` = Comfirmed<br>`F` = Failed |
| 4 | `CreateDate` | Request Creation Date | Date | 8 | - |  |  |
| 5 | `CreateTime` | Request Creation Time | Int | 11 | - |  |  |
| 6 | `LstUpdDate` | Latest Update Date | Date | 8 | - |  |  |
| 7 | `LstUpdTime` | Latest Update Time | Int | 11 | - |  |  |
| 8 | `UserSign` | Latest Update User Code | nVarChar | 8 | - |  |  |
| 9 | `Port` | Port | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
