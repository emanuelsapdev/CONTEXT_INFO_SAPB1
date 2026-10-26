# CUVE - Formulas

- **Tabla:** CUVE
- **Descripción:** Formulas
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CUVE.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IndexID` | Index | Int | 11 | - |  |  |
| 2 | `EName` | Formula Name | nVarChar | 100 | - |  |  |
| 3 | `EString` | Formula | Text | 16 | - |  |  |
| 4 | `EDescript` | Description | Text | 16 | - |  |  |
| 5 | `DelayTime` | Start time delay | nVarChar | 10 | - |  |  |
| 6 | `Status` | Status | Int | 11 | - |  |  |
| 7 | `CreateTS` | Create Time | Int | 11 | - |  |  |
| 8 | `UpdateTS` | Update Time | Int | 11 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IndexID |
| ENAME_K | Yes | EName |
