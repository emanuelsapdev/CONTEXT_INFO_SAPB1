# HEM5 - Employee Data Ownership Authorization

- **Tabla:** HEM5
- **Descripción:** Employee Data Ownership Authorization
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HEM5.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee No. | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `Object` | The Object Number | nVarChar | 20 | - |  |  |
| 3 | `Peer` | Peer Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 4 | `Manager` | Manager Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 5 | `Subord` | Subordinate Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 6 | `Dept` | Department Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 7 | `Branch` | Branch Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 8 | `Team` | Team Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 9 | `AC` | Cache Access Counter | Int | 11 | - | 0 |  |
| 10 | `Cmpny` | Company Authorization | VarChar | 1 | - | N | `F` = Full<br>`R` = Read Only<br>`N` = None<br>`U` = Undefined Type |
| 11 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, Object |
