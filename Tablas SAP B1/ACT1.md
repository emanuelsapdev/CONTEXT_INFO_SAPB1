# ACT1 - Service Contract - Items

- **Tabla:** ACT1
- **Descripción:** Service Contract - Items
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACT1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ContractID` | Contract No. | Int | 11 | [OCTR](OCTR.md) |  |  |
| 2 | `Line` | Row | Int | 11 | - |  |  |
| 3 | `ManufSN` | Mfr. Serial No. | nVarChar | 36 | - |  |  |
| 4 | `InternalSN` | Serial Number | nVarChar | 36 | - |  |  |
| 5 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 6 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 7 | `ItemGroup` | Item Group | Int | 6 | [OITB](OITB.md) |  |  |
| 8 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 9 | `EndDate` | End Date | Date | 8 | - |  |  |
| 10 | `ItmGrpName` | Item Group Name | nVarChar | 20 | - |  |  |
| 11 | `InsID` | Customer Equipment Card ID | Int | 11 | [OINS](OINS.md) |  |  |
| 12 | `TermDate` | Termination Date | Date | 8 | - |  |  |
| 13 | `LogInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 14 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ContractID, Line, LogInstanc |
