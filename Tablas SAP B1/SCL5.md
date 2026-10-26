# SCL5 - Service Call Activities

- **Tabla:** SCL5
- **Descripción:** Service Call Activities
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCL5.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SrvcCallId` | Service Call No. | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `Line` | Row | Int | 6 | - | -1 |  |
| 3 | `ClgID` | Activity Code | Int | 11 | [OCLG](OCLG.md) |  |  |
| 4 | `ObjectType` | Object Type | nVarChar | 20 | - | 191 |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 6 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `UserSign2` | User Signature 2 | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 10 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 11 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SrvcCallId, Line |
