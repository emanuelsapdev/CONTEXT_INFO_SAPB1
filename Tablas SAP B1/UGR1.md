# UGR1 - Group Authorization

- **Tabla:** UGR1
- **Descripción:** Group Authorization
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UGR1.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GroupLink` | Group Link | Int | 6 | [OUGR](OUGR.md) |  |  |
| 2 | `PermId` | Authorization ID | nVarChar | 20 | [OUPT](OUPT.md) |  |  |
| 3 | `Permission` | Authorization | VarChar | 1 | - | N | `V` = Various<br>`F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | GroupLink, PermId |
