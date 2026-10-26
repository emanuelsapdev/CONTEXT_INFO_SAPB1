# TAASF - Result of TaaS Tax Code Fix

- **Tabla:** TAASF
- **Descripción:** Result of TaaS Tax Code Fix
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TAASF.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 2 | `Internal` | Internal Number | Int | 11 | - |  |  |
| 3 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 4 | `DocDate` | Doc. Date | Date | 8 | - |  |  |
| 5 | `StaCode` | Tax Authorities Code | nVarChar | 8 | - |  |  |
| 6 | `StaType` | Tax Authorities Type | Int | 11 | - |  |  |
| 7 | `OldRate` | Old Rate | Num | 19.6 | - |  |  |
| 8 | `NewRate` | New Rate | Num | 19.6 | - |  |  |
| 9 | `FixType` | Fix Type | VarChar | 1 | - |  |  |
| 10 | `IsOK` | Is OK | VarChar | 1 | - |  |  |
| 11 | `Descr` | Description | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| DUMMY | Yes | LogInstanc, Internal |
