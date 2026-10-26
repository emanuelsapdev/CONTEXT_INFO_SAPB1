# SCL1 - Service Call Solutions - Rows

- **Tabla:** SCL1
- **Descripción:** Service Call Solutions - Rows
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCL1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `srvcCallID` | Service Call No. | Int | 11 | [OSCL](OSCL.md) |  |  |
| 2 | `line` | Row No. | Int | 6 | - | -1 |  |
| 3 | `solutionID` | Solution ID | Int | 11 | [OSLT](OSLT.md) |  |  |
| 4 | `objType` | Object Type | nVarChar | 20 | - | 191 |  |
| 5 | `logInstanc` | Log Instance | Int | 11 | - |  |  |
| 6 | `userSign` | Creating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 7 | `createDate` | Creation Date | Date | 8 | - |  |  |
| 8 | `userSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `updateDate` | Date of Update | Date | 8 | - |  |  |
| 10 | `VisOredr` | Visual Order | Int | 11 | - |  |  |
| 11 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | srvcCallID, line |
