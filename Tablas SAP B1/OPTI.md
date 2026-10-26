# OPTI - Point of Issue

- **Tabla:** OPTI
- **Descripción:** Point of Issue
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPTI.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 5 | - |  |  |
| 2 | `Desc` | Description | nVarChar | 100 | - |  |  |
| 3 | `Type` | Type | VarChar | 1 | - | P | `P` = Domestic Printing<br>`E` = Domestic Electronic<br>`F` = Fiscal<br>`X` = Export Printing<br>`T` = Export Electronic |
| 4 | `SOpDate` | Start Operating Date | Date | 8 | - |  |  |
| 5 | `EndOpDate` | End Operating Date | Date | 8 | - |  |  |
| 6 | `Remarks` | Remarks | nVarChar | 100 | - |  |  |
| 7 | `EDocExpFrm` | Electronic Doc. Export Format | Int | 11 | - |  |  |
| 8 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 9 | `EDocGenTyp` | Electronic Doc. Generation Type | VarChar | 1 | - |  | `N` = Not Relevant<br>`G` = Generate<br>`L` = CAEA - Generate Later |
| 10 | `CAEARqtFrm` | CAEA Request Format | Int | 11 | - |  |  |
| 11 | `Regime` | Regime of eDoc Format | VarChar | 1 | - |  | `1` = RG2485<br>`2` = RG2904 |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
