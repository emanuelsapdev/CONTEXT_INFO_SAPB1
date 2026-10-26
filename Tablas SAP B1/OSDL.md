# OSDL - Sensitive Personal Data Access Log

- **Tabla:** OSDL
- **Descripción:** Sensitive Personal Data Access Log
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSDL.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DataSubjct` | Data Subject Type | VarChar | 1 | - |  | `1` = OHEM<br>`2` = OCRD<br>`3` = OUSR<br>`4` = OCPR<br>`6` = OUDO |
| 3 | `SubjctKey` | Data Subject Key | nVarChar | 100 | - |  |  |
| 4 | `DataTable` | Data Table | nVarChar | 21 | - |  |  |
| 5 | `TblKeyCnt` | Data Table Key Count | Int | 11 | - |  |  |
| 6 | `KeyVal1` | Key Value 1 | nVarChar | 100 | - |  |  |
| 7 | `KeyVal2` | Key Value 2 | nVarChar | 100 | - |  |  |
| 8 | `KeyVal3` | Key Value 3 | nVarChar | 100 | - |  |  |
| 9 | `KeyVal4` | Key Value 4 | nVarChar | 100 | - |  |  |
| 10 | `Property` | Property Name | nVarChar | 50 | - |  |  |
| 11 | `UserSign` | Access User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 12 | `AccessDate` | Access Date | Int | 11 | - |  |  |
| 13 | `AccessTime` | Access Time | Int | 11 | - |  |  |
| 14 | `AccessChnl` | Access Channel | VarChar | 1 | - |  | `U` = UI<br>`D` = DI<br>`B` = Browser Access<br>`W` = Personal Data Management Wizard<br>`A` = Bank File |
| 15 | `Version` | Version | nVarChar | 13 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
