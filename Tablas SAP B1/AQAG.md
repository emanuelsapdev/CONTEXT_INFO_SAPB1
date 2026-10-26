# AQAG - Query Authorization Groups - Log

- **Tabla:** AQAG
- **Descripción:** Query Authorization Groups - Log
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AQAG.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AUTHGRPID` | Query Authorization Group ID | Int | 11 | - |  |  |
| 2 | `AUTHGRPCD` | Group Code | nVarChar | 50 | - |  |  |
| 3 | `AUTHGRPN` | Group Description | nVarChar | 254 | - |  |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `UserSign` | Item Created By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UserSign2` | Item Updated By | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 8 | `CreateDate` | Date of Create | Date | 8 | - |  |  |
| 9 | `Deleted` | Deleted Field | VarChar | 1 | - | N |  |
| 10 | `SnapShotID` | Snapshot ID | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AUTHGRPID, LogInstanc |
