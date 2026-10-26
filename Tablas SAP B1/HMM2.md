# HMM2 - Child Table of OHHM

- **Tabla:** HMM2
- **Descripción:** Child Table of OHHM
- **Cantidad de campos:** 4
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/HMM2.html

## Campos (4)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OHMM](OHMM.md) |  |  |
| 2 | `LineNum` | Child No. | Int | 11 | - |  |  |
| 3 | `VerType` | Version Type | VarChar | 1 | - |  | `H` = SAP HANA Version<br>`A` = SAP Business One Analytics Powered by HANA Version<br>`B` = SAP Business One Version |
| 4 | `Ver` | Version | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
