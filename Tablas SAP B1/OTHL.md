# OTHL - Thresholds

- **Tabla:** OTHL
- **Descripción:** Thresholds
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTHL.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `RecType` | Report Type | VarChar | 1 | - | A | `A` = Annual Invoice Declaration<br>`B` = Blacklist Country |
| 3 | `EffecFrom` | Effective From | Date | 8 | - |  |  |
| 4 | `Company` | Company | nVarChar | 20 | - |  |  |
| 5 | `PrivInv` | Private - Invoice | nVarChar | 20 | - |  |  |
| 6 | `PrivJE` | Private - Journal Entry | nVarChar | 20 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 9 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 12 | `Tourism` | Tourism | nVarChar | 20 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
