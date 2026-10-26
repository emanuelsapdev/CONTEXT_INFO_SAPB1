# JWT1 - User Authorization

- **Tabla:** JWT1
- **Descripción:** User Authorization
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/JWT1.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `UserLink` | USER LINK | nVarChar | 254 | [OJWT](OJWT.md) |  |  |
| 2 | `PermId` | Authorization ID | nVarChar | 20 | - |  |  |
| 3 | `CalcView` | CALVIEW ID | nVarChar | 254 | - |  |  |
| 4 | `Permission` | Authorization | VarChar | 1 | - | N | `V` = Various<br>`F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserLink, CalcView |
