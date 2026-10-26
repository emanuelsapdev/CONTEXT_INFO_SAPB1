# ASC1 - Service Call Solutions - History

- **Tabla:** ASC1
- **Descripción:** Service Call Solutions - History
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ASC1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `srvcCallID` | Service Call No. - History | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `line` | Row Number - History | Int | 6 | - | -1 |  |
| 3 | `solutionID` | Solution ID - History | Int | 11 | [OSLT](OSLT.md) |  |  |
| 4 | `objType` | Object Type - History | nVarChar | 20 | - | 191 |  |
| 5 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 6 | `userSign` | Creating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `createDate` | Creation Date - History | Date | 8 | - |  |  |
| 8 | `userSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `updateDate` | Date of Update - History | Date | 8 | - |  |  |
| 10 | `VisOredr` | Visual Order | Int | 11 | - |  |  |
| 11 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | srvcCallID, line, logInstanc |
