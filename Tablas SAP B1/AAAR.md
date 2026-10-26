# AAAR - Substitute Authorizer

- **Tabla:** AAAR
- **Descripción:** Substitute Authorizer
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AAAR.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `AuthrID` | Authorizer ID | Int | 11 | [OUSR](OUSR.md) |  |  |
| 3 | `SubsttID` | Substitute Authorizer ID | Int | 11 | [OUSR](OUSR.md) |  |  |
| 4 | `FromDate` | From Date | Date | 8 | - |  |  |
| 5 | `ToDate` | To Date | Date | 8 | - |  |  |
| 6 | `WtmCode` | Approval Template Code | Int | 11 | [OWTM](OWTM.md) |  |  |
| 7 | `Active` | Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `CreateDate` | Date Created | Date | 8 | - |  |  |
| 9 | `CreateTS` | Creatn Time - Incl. Secs | Int | 11 | - |  |  |
| 10 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 11 | `UserSign2` | User Signature 2 | Int | 6 | - |  |  |
| 12 | `Applied` | Substitute Action Performed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `UpdateDate` | Update Date | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
