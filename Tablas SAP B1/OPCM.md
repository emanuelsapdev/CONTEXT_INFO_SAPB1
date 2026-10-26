# OPCM - POS/Cash Register

- **Tabla:** OPCM
- **Descripción:** POS/Cash Register
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPCM.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `IdCode` | Identification Code | nVarChar | 50 | - |  |  |
| 3 | `PosCode` | Point of Service Code | nVarChar | 6 | - |  |  |
| 4 | `PosDesc` | Point of Service Description | nVarChar | 100 | - |  |  |
| 5 | `CrCode` | Cash Register Code | nVarChar | 20 | - |  |  |
| 6 | `CrDesc` | Cash Register Description | nVarChar | 100 | - |  |  |
| 7 | `Remarks` | Remarks | nVarChar | 250 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| ID_CODE | Yes | IdCode |
| POC_CR | Yes | PosCode, CrCode |
