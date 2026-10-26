# HEM1 - Absence Information

- **Tabla:** HEM1
- **Descripción:** Absence Information
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HEM1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `empID` | Employee ID | Int | 11 | [OHEM](OHEM.md) |  |  |
| 2 | `line` | Absence Information Row | Int | 6 | - |  |  |
| 3 | `fromDate` | Absence from | Date | 8 | - |  |  |
| 4 | `toDate` | Absence to | Date | 8 | - |  |  |
| 5 | `reason` | Reason | nVarChar | 20 | - |  |  |
| 6 | `approvedBy` | Approved By | nVarChar | 20 | - |  |  |
| 7 | `cnfrmrNum` | Confirmer Number | Int | 11 | [OHEM](OHEM.md) |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `type` | Absence Type | Int | 11 | [PMC5](PMC5.md) |  |  |
| 10 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 11 | `EnType` | Encrypt Absence Type | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | empID, line |
