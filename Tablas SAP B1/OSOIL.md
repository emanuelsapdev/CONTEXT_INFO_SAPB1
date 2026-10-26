# OSOIL - Statement of Import Wizard Run

- **Tabla:** OSOIL
- **Descripción:** Statement of Import Wizard Run
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSOIL.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SOIWNum` | Statement No. | nVarChar | 100 | - |  |  |
| 2 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 3 | `SOINum` | SOI | Int | 11 | - |  |  |
| 4 | `AbsEntry` | Abs Entry | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SOIWNum |
| SECONDARY | Yes | AbsEntry |
