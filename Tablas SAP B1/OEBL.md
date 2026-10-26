# OEBL - E-Balance

- **Tabla:** OEBL
- **Descripción:** E-Balance
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEBL.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `WizardName` | Wizard Name | nVarChar | 100 | - |  |  |
| 3 | `Status` | Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Saved |
| 4 | `CreateDate` | Create Date | Date | 8 | - |  |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
