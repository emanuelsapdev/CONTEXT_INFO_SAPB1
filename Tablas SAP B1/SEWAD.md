# SEWAD - SEWAD

- **Tabla:** SEWAD
- **Descripción:** SEWAD
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SEWAD.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Absolute Entry | Int | 11 | - |  |  |
| 2 | `DbName` | DB Name (common/company) | nVarChar | 100 | - |  |  |
| 3 | `AddonId` | Addon ID | Int | 11 | - |  |  |
| 4 | `AddonName` | Addon Name | nVarChar | 128 | - |  |  |
| 5 | `AddonVer` | Addon Version | nVarChar | 12 | - |  |  |
| 6 | `NameSpace` | Partner Name Space | nVarChar | 20 | - |  |  |
| 7 | `PartName` | Partner Name | nVarChar | 40 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| DBNAME | No | DbName |
