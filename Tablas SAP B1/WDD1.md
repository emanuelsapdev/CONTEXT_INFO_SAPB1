# WDD1 - Documents for Approval - Authorizers

- **Tabla:** WDD1
- **Descripción:** Documents for Approval - Authorizers
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WDD1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WddCode` | Internal ID | Int | 11 | - |  |  |
| 2 | `StepCode` | Stage Key | Int | 11 | [OWST](OWST.md) |  |  |
| 3 | `UserID` | Authorizer Code | Int | 11 | [OUSR](OUSR.md) |  |  |
| 4 | `Status` | Status | VarChar | 1 | - | W | `W` = Pending<br>`Y` = Approved<br>`N` = Rejected |
| 5 | `Remarks` | Remarks | nVarChar | 254 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `CreateDate` | Request Date | Date | 8 | - |  |  |
| 8 | `CreateTime` | Request Time | Int | 6 | - |  |  |
| 9 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 10 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 11 | `SortId` | Sort Code | Int | 6 | - |  |  |
| 12 | `AuthUpdDat` | Authorizer last update date | Date | 8 | - |  |  |
| 13 | `AuthUpdTim` | Authorizer last update time | Int | 11 | - |  |  |
| 14 | `Substt` | Substitute Authorizer User ID | Int | 11 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WddCode, StepCode, UserID |
