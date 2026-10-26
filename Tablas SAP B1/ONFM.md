# ONFM - Nota Fiscal Model

- **Tabla:** ONFM
- **Descripción:** Nota Fiscal Model
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ONFM.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | NF Model ID | nVarChar | 6 | - |  |  |
| 2 | `NfmName` | NF Model Name | nVarChar | 20 | - |  |  |
| 3 | `NfmDescrip` | NF Model Description | nVarChar | 100 | - |  |  |
| 4 | `UserSign` | User Signature - Create | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 7 | `NfmCode` | NF Model Code | nVarChar | 10 | - |  |  |
| 8 | `NfmTW` | Tax Wizard Relevant | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
