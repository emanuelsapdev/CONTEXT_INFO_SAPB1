# CRDC - BP - Communication Means

- **Tabla:** CRDC
- **Descripción:** BP - Communication Means
- **Cantidad de campos:** 3
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CRDC.html

## Campos (3)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 2 | `CommMeanId` | Communication Mean ID | Int | 11 | [OCMM](OCMM.md) |  |  |
| 3 | `Select` | Select | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CardCode, CommMeanId |
