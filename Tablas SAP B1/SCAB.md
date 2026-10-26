# SCAB - Appl CABs

- **Tabla:** SCAB
- **Descripción:** Appl CABs
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCAB.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Version` | Version | Int | 11 | - |  |  |
| 2 | `Flags` | Flags | nVarChar | 50 | - | NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN |  |
| 3 | `ApplCab` | Appl. CAB | Text | 16 | - |  |  |
| 4 | `DbCab` | Metadata CAB | Text | 16 | - |  |  |
| 5 | `ComOBSCab` | Com OBS CAB | Text | 16 | - |  |  |
| 6 | `ComUICab` | Com UI CAB | Text | 16 | - |  |  |
| 7 | `ApplCab64` | Appl. CAB (64bit) | Text | 16 | - |  |  |
| 8 | `DbCab64` | Metadata CAB (64bit) | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Version |
