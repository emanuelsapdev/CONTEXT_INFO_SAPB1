# RDFL - Document Standards

- **Tabla:** RDFL
- **Descripción:** Document Standards
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RDFL.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DoumntDode` | Code | nVarChar | 4 | - |  |  |
| 2 | `UserId` | User Signature | Int | 11 | - |  |  |
| 3 | `DfltReport` | Standard Report | nVarChar | 8 | - |  |  |
| 4 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) | -1 |  |
| 5 | `DfltSeq` | Standard Sequence | Int | 11 | - |  |  |
| 6 | `TYPE` | Type | VarChar | 1 | - | L | `L` = Layout<br>`P` = Print Sequence |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DoumntDode, UserId, CardCode |
| CODE | No | DoumntDode |
