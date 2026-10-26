# UVE1 - Formulas

- **Tabla:** UVE1
- **Descripción:** Formulas
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UVE1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 2 | `IndexID` | Index | Int | 11 | [CUVE](CUVE.md) |  |  |
| 3 | `LkupObject` | Lookup Object | nVarChar | 254 | - |  |  |
| 4 | `BObject` | Business Object | nVarChar | 254 | - |  |  |
| 5 | `LkupField` | Lookup Field | nVarChar | 254 | - |  |  |
| 6 | `BField` | Database Field | nVarChar | 254 | - |  |  |
| 7 | `CmprWith` | Compare With | Int | 6 | - | 1 | `1` = UI Field<br>`2` = Constant |
| 8 | `LkupValue` | Lookup Value | nVarChar | 254 | - |  |  |
| 9 | `CreateTS` | Create Time | Int | 11 | - |  |  |
| 10 | `UpdateTS` | Update Time | Int | 11 | - |  |  |
| 11 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 14 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IntrnalKey |
